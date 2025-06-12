This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!


##############################################################

Note utili per i prossimi sviluppi Google Cloud:

- se vuoi deployare la tua app su cloud run con una pipeline CICD basata su repository bisogna fare le seguenti cose:
    - creare un service account che si occupi del deploy
    - collegarlo al repository GitHub: creare una chiave json, inserirla nei secrets del repository
    - creare un file deploy.yaml apposito che istruisca build e deploy automatici e contenga altre info utili (come il secret del passo precedente)
    - assegnare al service account coinvolto una lunga lista di permessi: ['roles/artifactregistry.admin', 'roles/artifactregistry.serviceAgent', 'roles/artifactregistry.writer', 'roles/cloudbuild.builds.builder', 'roles/cloudbuild.serviceAgent', 'roles/containeranalysis.ServiceAgent', 'roles/containerregistry.ServiceAgent', 'roles/editor', 'roles/iam.serviceAccountUser', 'roles/logging.logWriter', 'roles/owner', 'roles/pubsub.serviceAgent', 'roles/run.admin', 'roles/run.invoker', 'roles/run.serviceAgent', 'roles/serviceusage.serviceUsageConsumer', 'roles/storage.admin'] 

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
