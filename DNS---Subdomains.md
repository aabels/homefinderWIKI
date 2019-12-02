## Creating a subdomain
A sub domain allows us to create any number of endpoints under the `rentwhiz.ca` domain name. Creating a subdomain and delegating the Name Server resolution to Cybera allows to us quickly create, remove, and change endpoints without affecting the main domain `rentwhiz.ca`

To add a subdomain, you first need to create a Hosted Zone in Cybera. You can do so by going to the Cybera RAC -> DNS -> Zones -> Create new Hosted Zone

Name: `<your_subdomain>.rentwhiz.ca.`
Email: `<your_email>`
Defaults for everything else.

Now that it is created, navigate to the zone and grab the `NS` (Name Server entries). You will need these to update your domain provider settings to delegate all domains `*.<your_subdomain>.rentwhiz.ca` to Cybera DNS.

Once at your domain management page, create a new NS record. For the name put `<your_subdomain>` and for the entry, put the NS values you copied from Cybera. Click save and wait for the changes to propagate (usually about 5-10 minutes)

