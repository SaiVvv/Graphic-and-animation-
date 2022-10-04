#include<GL/glu.h>
#include <GL/glut.h>


void MyInit()
{
   glClearColor(0,0,1,1);
}

void draw()
{
  glClear(GL_COLOR_BUFFER_BIT);

 glBegin(0);
 glEnd();

  glFlush();
}
int main(int c, char *v[])
{
    glutInit(&c,v);
    glutInitWindowPosition(300,300);
    glutInitWindowSize(400,400);
    glutInitDisplayMode(GLUT_RGB | GLUT_SINGLE);
    glutCreateWindow("My first window");

    MyInit();

    glutDisplayFunc(draw);
    glutMainLoop();

    return 0;
}
