Components
-> its a piece of UI which consists of its own logic and appearance.
-> React apps are made up of this Components.

example
function Mybutton(){
    return (
        <button> This is button </button>
    );
}



you can use this component in other components for example

export default function myapp() {
    return(
        <div>
          <h1> Welcome to my app </h1>
        <Mybutton />
        </div>
    );  
}



displaying the data 

const user = {
    name : 'Hedy Lamrar',
    imageURL : 'https://i.imgur.com/yXOvdOSs.jpg'
    imageSize: 90,
};

export default function Profile() {
    return (
        <h1> {user.name} </h1>
        <img
        classname='avatar',
        src= {user.imageURL}
        alt = {'Photo of' + user.name }
        style = {{
         width: user.imageSize,
          height: user.imageSize
        }}
        
       />
    );
}