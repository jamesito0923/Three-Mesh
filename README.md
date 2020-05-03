# Three-Mesh-UI
Three-Mesh-UI helps in easily adding user interface in a Three.js scene, in order to make better VR experiences

![preview three-mesh-ui](https://felixmariotto.s3.eu-west-3.amazonaws.com/github_preview.gif)

## Demos
It's over there : https://three-mesh-ui.herokuapp.com

# overview

### MeshUIComponent:
This is the base object to which all the other components delegate.  
It store some generic information about any subcomponent: id, parent, children.
It also store getters functions, whose job are to find a property in this component *or its parents.* When it does not find a property in this component or its parent, it returns the default value. MeshUIComponent also has a "set" method, which updates the component properties, take actions accordingly if necessary, then call the update function of the component whose parameters changed. All the subcomponents internally call MeshUIComponent.set with the parameters you pass when constructing a new instance, so you should try to pass all the paramters on construction if possible, for better performance.
