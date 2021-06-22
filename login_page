from flask import Flask,request,render_template


app = Flask(__name__)


@app.route('/')
def hello_world():
    return render_template("login_page.html")
database={'Himanshu':'123','Aditya':'456'}

@app.route('/form_login',methods=['POST','GET'])
def login():
    name1=request.form['username']
    pwd=request.form['password']
    if name1 not in database:
	    return render_template('login_page.html',info='Invalid User')
    else:
        if database[name1]!=pwd:
            return render_template('login_page.html',info='Invalid Password')
        else:
	         return render_template('home.html',name=name1)

if __name__ == '__main__':
    app.run()
