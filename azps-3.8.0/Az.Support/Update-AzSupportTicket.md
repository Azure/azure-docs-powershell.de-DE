---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 160d6b4d4a8505c99d5bfcb4c535ec7bbb3b6dd3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996361"
---
# <span data-ttu-id="9e75b-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="9e75b-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="9e75b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e75b-102">SYNOPSIS</span></span>
<span data-ttu-id="9e75b-103">Support-Ticket für Updates.</span><span class="sxs-lookup"><span data-stu-id="9e75b-103">Updates support ticket.</span></span>

## <span data-ttu-id="9e75b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e75b-104">SYNTAX</span></span>

### <span data-ttu-id="9e75b-105">UpdateByNameWithContactDetailParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e75b-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e75b-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e75b-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e75b-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e75b-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e75b-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e75b-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e75b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e75b-109">DESCRIPTION</span></span>
<span data-ttu-id="9e75b-110">Verwenden Sie dieses Cmdlet, um den Schweregrad, den Status oder die Kundenkontakt Details eines Support Tickets zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9e75b-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="9e75b-111">Beachten Sie, dass das Aktualisieren des Schweregrads oder des Status eines Support Tickets nicht zulässig ist, wenn das Ticket einem Supporttechniker zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9e75b-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="9e75b-112">Wenn Sie den Schweregrad oder den Status nach der ticketzuweisung aktualisieren möchten, wenden Sie sich an den Supporttechniker, indem Sie eine Mitteilung über das Ticket senden.</span><span class="sxs-lookup"><span data-stu-id="9e75b-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="9e75b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e75b-113">EXAMPLES</span></span>

### <span data-ttu-id="9e75b-114">Beispiel 1: Update des Schweregrads des Support Tickets</span><span class="sxs-lookup"><span data-stu-id="9e75b-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9e75b-115">Beispiel 2: Status des Support Tickets aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9e75b-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9e75b-116">Beispiel 3: Aktualisieren Sie die Kontaktdetails des Support Tickets, indem Sie Kontaktobjekt angeben.</span><span class="sxs-lookup"><span data-stu-id="9e75b-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9e75b-117">Beispiel 4: Update des Schweregrads des Support-Tickets durch Piping Support Ticket-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9e75b-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9e75b-118">Beispiel 5: Aktualisieren Sie die Kontaktdetails des Support Tickets, indem Sie einzelne kontaktparameter angeben.</span><span class="sxs-lookup"><span data-stu-id="9e75b-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9e75b-119">Beispiel 6: Aktualisieren des Status des Support Tickets durch das Rohrleitungs Support-Ticket Objekt.</span><span class="sxs-lookup"><span data-stu-id="9e75b-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="9e75b-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e75b-120">PARAMETERS</span></span>

### <span data-ttu-id="9e75b-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9e75b-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="9e75b-122">Weitere e-Mail-Adressen.</span><span class="sxs-lookup"><span data-stu-id="9e75b-122">Additional email addresses.</span></span>
<span data-ttu-id="9e75b-123">Die hier aufgelisteten e-Mail-Adressen werden auf jede Korrespondenz über das Support-Ticket kopiert.</span><span class="sxs-lookup"><span data-stu-id="9e75b-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="9e75b-124">-CustomerContactDetail</span></span>
<span data-ttu-id="9e75b-125">Aktualisieren Sie die Kontaktinformationen auf Supportticket.</span><span class="sxs-lookup"><span data-stu-id="9e75b-125">Update Contact details on SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: UpdateByNameWithContactObjectParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="9e75b-126">-CustomerCountry</span></span>
<span data-ttu-id="9e75b-127">Kunden Land.</span><span class="sxs-lookup"><span data-stu-id="9e75b-127">Customer country.</span></span>
<span data-ttu-id="9e75b-128">Dies muss eine gültige ISO-Alpha-3-Landesvorwahl (ISO 3166) sein.</span><span class="sxs-lookup"><span data-stu-id="9e75b-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="9e75b-129">-CustomerFirstName</span></span>
<span data-ttu-id="9e75b-130">Name des Kunden Vornamens</span><span class="sxs-lookup"><span data-stu-id="9e75b-130">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="9e75b-131">-CustomerLastName</span></span>
<span data-ttu-id="9e75b-132">Nachname des Kunden</span><span class="sxs-lookup"><span data-stu-id="9e75b-132">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="9e75b-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="9e75b-134">Kundentelefonnummer.</span><span class="sxs-lookup"><span data-stu-id="9e75b-134">Customer phone number.</span></span>
<span data-ttu-id="9e75b-135">Dies ist erforderlich, wenn die bevorzugte Kontaktmethode Telefon ist.</span><span class="sxs-lookup"><span data-stu-id="9e75b-135">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="9e75b-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="9e75b-137">Kunden bevorzugte Support Sprache.</span><span class="sxs-lookup"><span data-stu-id="9e75b-137">Customer preferred support language.</span></span>
<span data-ttu-id="9e75b-138">Hierbei muss es sich um einen gültigen sprach Fortsetzungs Code für eine der hier aufgeführten unterstützten Sprachen handeln https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="9e75b-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="9e75b-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="9e75b-140">Bevorzugte Zeitzone des Kunden.</span><span class="sxs-lookup"><span data-stu-id="9e75b-140">Customer preferred time zone.</span></span>
<span data-ttu-id="9e75b-141">Dies muss ein gültiger System.TimeZoneInfo.ID-Wert sein.</span><span class="sxs-lookup"><span data-stu-id="9e75b-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9e75b-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="9e75b-143">Primäre e-Mail-Adresse des Kunden.</span><span class="sxs-lookup"><span data-stu-id="9e75b-143">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e75b-144">-DefaultProfile</span></span>
<span data-ttu-id="9e75b-145">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e75b-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-146">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9e75b-146">-InputObject</span></span>
<span data-ttu-id="9e75b-147">Supportticket-Ressourcenobjekt, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9e75b-147">SupportTicket resource object that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: UpdateByInputObjectWithContactDetailParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-148">-Name</span><span class="sxs-lookup"><span data-stu-id="9e75b-148">-Name</span></span>
<span data-ttu-id="9e75b-149">Der Name der vom Cmdlet aktualisierten Supportticket-Ressource.</span><span class="sxs-lookup"><span data-stu-id="9e75b-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByNameWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="9e75b-150">-PreferredContactMethod</span></span>
<span data-ttu-id="9e75b-151">Bevorzugte Kontaktmethode.</span><span class="sxs-lookup"><span data-stu-id="9e75b-151">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-152">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="9e75b-152">-Severity</span></span>
<span data-ttu-id="9e75b-153">Update Schweregrad von Supportticket.</span><span class="sxs-lookup"><span data-stu-id="9e75b-153">Update Severity of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-154">-Status</span><span class="sxs-lookup"><span data-stu-id="9e75b-154">-Status</span></span>
<span data-ttu-id="9e75b-155">Update Status von Supportticket.</span><span class="sxs-lookup"><span data-stu-id="9e75b-155">Update Status of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Status
Parameter Sets: (All)
Aliases:
Accepted values: Open, Closed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e75b-156">-Confirm</span></span>
<span data-ttu-id="9e75b-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e75b-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e75b-158">-WhatIf</span></span>
<span data-ttu-id="9e75b-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e75b-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e75b-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e75b-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e75b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e75b-161">CommonParameters</span></span>
<span data-ttu-id="9e75b-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e75b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e75b-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e75b-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e75b-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e75b-164">INPUTS</span></span>

### <span data-ttu-id="9e75b-165">Microsoft. Azure. Commands. Support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="9e75b-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="9e75b-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e75b-166">OUTPUTS</span></span>

### <span data-ttu-id="9e75b-167">Microsoft. Azure. Commands. Support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="9e75b-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="9e75b-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e75b-168">NOTES</span></span>

## <span data-ttu-id="9e75b-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e75b-169">RELATED LINKS</span></span>
