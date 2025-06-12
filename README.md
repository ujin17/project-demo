// This test case for automation login page demo example usig Cypress.

/// <reference types="Cypress" />
describe('this is login page',()=>{

   it('encounter login page for valid credential',()=>{
    cy.visit('https://mv-i.github.io/me/projects/login/dummy.html')
    cy.get('#linkCreateAccount').click()
    cy.get('#signupUsername').type('hello')
    cy.get('#signupEmail').type('ujinsekar143@gmail.com')
    cy.get('#signupPassword').type('Ujinsekar@17')
    cy.get('#signupPassword2').type('Ujinsekar@17')
    cy.wait(3000)
    cy.get('#createAccount > .form__button').click()
    cy.get('#linkLoginCA').click()
    cy.get('#loginUsernameEmail').type('ujinsekar143@gmail.com')
    cy.get('#loginPassword').type('Ujinsekar@17')
    cy.wait(3000)
    cy.get('#login > .form__button').click();
    })

})
