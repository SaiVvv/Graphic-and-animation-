#include<GL/glut.h>
#include<math.h>

double parr[8];

void init()
{
    glClear(GL_COLOR_BUFFER_BIT);
    glClearColor(0,0,0,1);
    glColor3f(1,0,1);
    gluOrtho2D(-500,500,-500,500); // Left,right,bottom,top

    // Polygon Default
    parr[0] = 10;  //x
    parr[1] = 10;  //y

    parr[2] = 200;
    parr[3] = 10;

    parr[4] = 150;
    parr[5] = 150;
}

void polygon()
{
    glColor3f(1,0,0);
    glBegin(GL_LINE_LOOP);
        glVertex2f(parr[0],parr[1]);
        glVertex2f(parr[2],parr[3]);

        glVertex2f(parr[4],parr[5]);

    glEnd();

    glFlush();
}

void drawCorodinates()
{
    glClear(GL_COLOR_BUFFER_BIT);

    glColor3f(1,1,1);
    glPointSize(4);

    glBegin(GL_LINES);
        glVertex2f(-500,0);
        glVertex2f(500,0);

        glVertex2f(0,500);
        glVertex2f(0,-500);
    glEnd();

    glColor3f(1,0,0);

    glBegin(GL_POINTS);
        glVertex2f(0,0);
    glEnd();

    glFlush();
}

// Shearing About X-Axis
void shearing_x()
{
     int shx = 2;

    for(int i=0;i<6;i=i+2)
    {
        parr[i] = parr[i] + shx*parr[i+1];
    }

    polygon();
}


// Shearing About Y-Axis
void shearing_y()
{
     int shy = 2;

    for(int i=1;i<6;i=i+2)
    {
        parr[i] = parr[i] + shy*parr[i-1];
    }

    polygon();
}

void menu(int ch)
{
        drawCorodinates();
    switch(ch)
    {
        case 1: polygon();
            break;

        case 6: shearing_x();
            break;
        case 7: shearing_y();
            break;
    }
}

int main(int argc,char **argv)
{
    glutInit(&argc,argv);
    glutInitWindowSize(500,500);
    glutInitWindowPosition(100,100);

    glutCreateWindow("2D Transformation");
    init();
    glutDisplayFunc(drawCorodinates);

    glutCreateMenu(menu);
        glutAddMenuEntry("1 Display Polygon",1);
        glutAddMenuEntry("6 Shearing About X-Axis",6);
        glutAddMenuEntry("7 Shearing About Y-Axiis",7);
    glutAttachMenu(GLUT_RIGHT_BUTTON);

    glutMainLoop();
    return 0;
}
