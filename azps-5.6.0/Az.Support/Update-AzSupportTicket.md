---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 5fac9eac7225364af7c884ab64a80d4299939ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945472"
---
# <span data-ttu-id="85087-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="85087-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="85087-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85087-102">SYNOPSIS</span></span>
<span data-ttu-id="85087-103">Aktualisiert das Supportticket.</span><span class="sxs-lookup"><span data-stu-id="85087-103">Updates support ticket.</span></span>

## <span data-ttu-id="85087-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85087-104">SYNTAX</span></span>

### <span data-ttu-id="85087-105">UpdateByNameWithContactDetailParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="85087-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85087-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85087-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85087-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="85087-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85087-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85087-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85087-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85087-109">DESCRIPTION</span></span>
<span data-ttu-id="85087-110">Verwenden Sie dieses Cmdlet, um den Schweregrad, den Status oder die Kontaktdetails eines Supporttickets zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="85087-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="85087-111">Beachten Sie, dass das Aktualisieren des Schweregrads oder Status eines Supporttickets nicht zulässig ist, wenn das Ticket einem Supporttechniker zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="85087-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="85087-112">Wenn Sie den Schweregrad oder Status nach der Ticketzuweisung aktualisieren möchten, wenden Sie sich an den Supporttechniker, indem Sie eine Kommunikation über das Ticket senden.</span><span class="sxs-lookup"><span data-stu-id="85087-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="85087-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85087-113">EXAMPLES</span></span>

### <span data-ttu-id="85087-114">Beispiel 1: Schweregrad des Supporttickets aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="85087-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="85087-115">Beispiel 2: Aktualisieren des Status des Supporttickets.</span><span class="sxs-lookup"><span data-stu-id="85087-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="85087-116">Beispiel 3: Aktualisieren Sie die Kontaktdetails des Supporttickets, indem Sie das Kontaktobjekt angeben.</span><span class="sxs-lookup"><span data-stu-id="85087-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="85087-117">Beispiel 4: Aktualisieren des Schweregrads des Supporttickets durch Piping-Supportticketobjekt.</span><span class="sxs-lookup"><span data-stu-id="85087-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="85087-118">Beispiel 5: Aktualisieren Sie die Kontaktdetails des Supporttickets, indem Sie einzelne Kontaktparameter angeben.</span><span class="sxs-lookup"><span data-stu-id="85087-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="85087-119">Beispiel 6: Aktualisieren des Status des Supporttickets durch Piping-Supportticketobjekt.</span><span class="sxs-lookup"><span data-stu-id="85087-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="85087-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="85087-120">PARAMETERS</span></span>

### <span data-ttu-id="85087-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="85087-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="85087-122">Weitere E-Mail-Adressen.</span><span class="sxs-lookup"><span data-stu-id="85087-122">Additional email addresses.</span></span>
<span data-ttu-id="85087-123">Die hier aufgeführten E-Mail-Adressen werden in jede Korrespondenz über das Supportticket kopiert.</span><span class="sxs-lookup"><span data-stu-id="85087-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="85087-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="85087-124">-CustomerContactDetail</span></span>
<span data-ttu-id="85087-125">Aktualisieren Sie kontaktdetails auf SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="85087-125">Update Contact details on SupportTicket.</span></span>

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

### <span data-ttu-id="85087-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="85087-126">-CustomerCountry</span></span>
<span data-ttu-id="85087-127">Kundenland.</span><span class="sxs-lookup"><span data-stu-id="85087-127">Customer country.</span></span>
<span data-ttu-id="85087-128">Dies muss ein gültiger ISO Alpha-3-Ländercode (ISO 3166) sein.</span><span class="sxs-lookup"><span data-stu-id="85087-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="85087-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="85087-129">-CustomerFirstName</span></span>
<span data-ttu-id="85087-130">Vorname des Kunden.</span><span class="sxs-lookup"><span data-stu-id="85087-130">Customer first name.</span></span>

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

### <span data-ttu-id="85087-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="85087-131">-CustomerLastName</span></span>
<span data-ttu-id="85087-132">Nachname des Kunden.</span><span class="sxs-lookup"><span data-stu-id="85087-132">Customer last name.</span></span>

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

### <span data-ttu-id="85087-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="85087-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="85087-134">Telefonnummer des Kunden.</span><span class="sxs-lookup"><span data-stu-id="85087-134">Customer phone number.</span></span>
<span data-ttu-id="85087-135">Dies ist erforderlich, wenn die bevorzugte Kontaktmethode das Telefon ist.</span><span class="sxs-lookup"><span data-stu-id="85087-135">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="85087-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="85087-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="85087-137">Bevorzugte Supportsprache des Kunden.</span><span class="sxs-lookup"><span data-stu-id="85087-137">Customer preferred support language.</span></span>
<span data-ttu-id="85087-138">Dies muss ein gültiger Sprachcode für eine der hier aufgeführten unterstützten Sprachen https://azure.microsoft.com/support/faq/ sein.</span><span class="sxs-lookup"><span data-stu-id="85087-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="85087-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="85087-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="85087-140">Vom Kunden bevorzugte Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="85087-140">Customer preferred time zone.</span></span>
<span data-ttu-id="85087-141">Dies muss ein gültiger System.TimeZoneInfo.Id sein.</span><span class="sxs-lookup"><span data-stu-id="85087-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="85087-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="85087-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="85087-143">Primäre E-Mail-Adresse des Kunden.</span><span class="sxs-lookup"><span data-stu-id="85087-143">Customer primary email address.</span></span>

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

### <span data-ttu-id="85087-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85087-144">-DefaultProfile</span></span>
<span data-ttu-id="85087-145">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85087-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85087-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85087-146">-InputObject</span></span>
<span data-ttu-id="85087-147">SupportTicket-Ressourcenobjekt, das dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="85087-147">SupportTicket resource object that this cmdlet updates.</span></span>

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

### <span data-ttu-id="85087-148">-Name</span><span class="sxs-lookup"><span data-stu-id="85087-148">-Name</span></span>
<span data-ttu-id="85087-149">Name der SupportTicket-Ressource, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="85087-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

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

### <span data-ttu-id="85087-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="85087-150">-PreferredContactMethod</span></span>
<span data-ttu-id="85087-151">Bevorzugte Kontaktmethode.</span><span class="sxs-lookup"><span data-stu-id="85087-151">Preferred contact method.</span></span>

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

### <span data-ttu-id="85087-152">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="85087-152">-Severity</span></span>
<span data-ttu-id="85087-153">Updateschweregrad von SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="85087-153">Update Severity of SupportTicket.</span></span>

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

### <span data-ttu-id="85087-154">-Status</span><span class="sxs-lookup"><span data-stu-id="85087-154">-Status</span></span>
<span data-ttu-id="85087-155">Updatestatus von SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="85087-155">Update Status of SupportTicket.</span></span>

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

### <span data-ttu-id="85087-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="85087-156">-Confirm</span></span>
<span data-ttu-id="85087-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85087-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85087-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85087-158">-WhatIf</span></span>
<span data-ttu-id="85087-159">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85087-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85087-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85087-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85087-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85087-161">CommonParameters</span></span>
<span data-ttu-id="85087-162">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85087-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85087-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85087-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85087-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85087-164">INPUTS</span></span>

### <span data-ttu-id="85087-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="85087-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="85087-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85087-166">OUTPUTS</span></span>

### <span data-ttu-id="85087-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="85087-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="85087-168">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="85087-168">NOTES</span></span>

## <span data-ttu-id="85087-169">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="85087-169">RELATED LINKS</span></span>
