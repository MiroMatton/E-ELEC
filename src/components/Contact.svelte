<div class="wrapper">
  <aside>
    <h2>contacteer ons</h2>
    <a href="tel:+32 69 420 666">+32 69 420 666</a>
    <a href="mailto: INFO@E-ELEC.BE">INFO@E-ELEC.BE</a>
  </aside>
  <section>
    <h2>stuur een bericht</h2>
    <form action="https://formsubmit.co/" method="POST">
      <div id="userGegevens">
        <input type="hidden" name="_next" value="#" />
        <input type="hidden" name="_captcha" value="false" />
        <input id="name" name="name" type="text" placeholder="naam" required />
        <input
          id="email"
          name="email"
          type="email"
          placeholder="E-mail"
          required
        />
      </div>
      <textarea placeholder="message" name="msg" id="msg" rows="1s" required />
      <button class="submit" type="submit">VERSTUUR</button>
    </form>
  </section>
</div>

<style lang="scss">
  @use "../styles/global";

  aside h2,
  section h2 {
    margin: 1rem 0;
    margin: 2rem 0;
  }

  aside {
    width: 40%;
    padding: 0 8rem 0 3rem;
    display: flex;
    flex-direction: column;

    a {
      margin-bottom: 0.5rem;
    }

    @media (max-width: global.$mobile) {
      text-align: center;
      padding: 0 0 1rem 0;
      background-color: global.$orange;
    }
  }

  section {
    width: 60%;
    h2 {
      @media (max-width: global.$mobile) {
        text-align: center;
      }
    }

    form {
      #userGegevens {
        display: flex;

        #name {
          width: 40%;
        }

        #email {
          width: 60%;
          margin-left: 2rem;
        }

        @media (max-width: global.$mobile) {
          flex-direction: column;

          #name,
          #email {
            width: 100%;
            margin-left: 0;
          }
        }
      }

      input,
      textarea {
        margin-bottom: 2rem;
        background: transparent;
        border: none;
        outline: none;
        border-bottom: 2px solid black;
        padding: 10px;
        width: 100%;
        resize: vertical;
      }

      .submit {
        background-color: black;
        color: white;
        border: none;
        padding: 0.5rem 1rem;
        margin: 1.5rem 0;
        font-size: 1rem;
        font-weight: 600;

        &:hover {
          background-color: global.$orange;
        }
      }
    }
  }
</style>
