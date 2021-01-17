---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460055"
---
# <span data-ttu-id="6ca71-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="6ca71-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="6ca71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ca71-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca71-103">Erstellt ein Supportkontaktprofilobjekt.</span><span class="sxs-lookup"><span data-stu-id="6ca71-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="6ca71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ca71-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca71-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ca71-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca71-106">Dies ist ein Hilfs-Cmdlet, mit dem Sie ein Supportkontaktprofilobjekt erstellen können, wenn Sie ein Supportticket erstellen oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6ca71-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="6ca71-107">Sie müssen die folgenden Parameter angeben, die für das Erstellen eines Supporttickets erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="6ca71-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="6ca71-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6ca71-108">EXAMPLES</span></span>

### <span data-ttu-id="6ca71-109">Beispiel 1: Erstellen eines Kontaktobjekts</span><span class="sxs-lookup"><span data-stu-id="6ca71-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="6ca71-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ca71-110">PARAMETERS</span></span>

### <span data-ttu-id="6ca71-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6ca71-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="6ca71-112">Die hier aufgelisteten E-Mail-Adressen werden nach Übereinstimmung mit dem Supportticket kopiert.</span><span class="sxs-lookup"><span data-stu-id="6ca71-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca71-113">-Country</span><span class="sxs-lookup"><span data-stu-id="6ca71-113">-Country</span></span>
<span data-ttu-id="6ca71-114">Land des Kunden.</span><span class="sxs-lookup"><span data-stu-id="6ca71-114">Customer country.</span></span>
<span data-ttu-id="6ca71-115">Dies muss ein gültiger ISO Alpha-3-Ländercode (ISO 3166) sein.</span><span class="sxs-lookup"><span data-stu-id="6ca71-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca71-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca71-116">-DefaultProfile</span></span>
<span data-ttu-id="6ca71-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ca71-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ca71-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="6ca71-118">-FirstName</span></span>
<span data-ttu-id="6ca71-119">Vorname des Kunden.</span><span class="sxs-lookup"><span data-stu-id="6ca71-119">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca71-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="6ca71-120">-LastName</span></span>
<span data-ttu-id="6ca71-121">Nachname des Kunden.</span><span class="sxs-lookup"><span data-stu-id="6ca71-121">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca71-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="6ca71-122">-PhoneNumber</span></span>
<span data-ttu-id="6ca71-123">Telefonnummer des Kunden.</span><span class="sxs-lookup"><span data-stu-id="6ca71-123">Customer phone number.</span></span>
<span data-ttu-id="6ca71-124">Dies ist erforderlich, wenn die bevorzugte Kontaktmethode "Telefon" ist.</span><span class="sxs-lookup"><span data-stu-id="6ca71-124">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca71-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="6ca71-125">-PreferredContactMethod</span></span>
<span data-ttu-id="6ca71-126">Bevorzugte Kontaktmethode.</span><span class="sxs-lookup"><span data-stu-id="6ca71-126">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: (All)
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca71-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="6ca71-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="6ca71-128">Bevorzugte Supportsprache des Kunden.</span><span class="sxs-lookup"><span data-stu-id="6ca71-128">Customer preferred support language.</span></span>
<span data-ttu-id="6ca71-129">Dies muss ein gültiger Code für andere Sprachen für eine der hier aufgeführten unterstützten Sprachen https://azure.microsoft.com/support/faq/ sein.</span><span class="sxs-lookup"><span data-stu-id="6ca71-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca71-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="6ca71-130">-PreferredTimeZone</span></span>
<span data-ttu-id="6ca71-131">Vom Kunden bevorzugte Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="6ca71-131">Customer preferred time zone.</span></span>
<span data-ttu-id="6ca71-132">Dies muss ein gültiger System.TimeZoneInfo.Id sein.</span><span class="sxs-lookup"><span data-stu-id="6ca71-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca71-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6ca71-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="6ca71-134">Primäre E-Mail-Adresse des Kunden.</span><span class="sxs-lookup"><span data-stu-id="6ca71-134">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca71-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ca71-135">-Confirm</span></span>
<span data-ttu-id="6ca71-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ca71-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca71-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6ca71-137">-WhatIf</span></span>
<span data-ttu-id="6ca71-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ca71-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ca71-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ca71-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca71-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca71-140">CommonParameters</span></span>
<span data-ttu-id="6ca71-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca71-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca71-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ca71-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca71-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6ca71-143">INPUTS</span></span>

### <span data-ttu-id="6ca71-144">Keine</span><span class="sxs-lookup"><span data-stu-id="6ca71-144">None</span></span>

## <span data-ttu-id="6ca71-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6ca71-145">OUTPUTS</span></span>

### <span data-ttu-id="6ca71-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="6ca71-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="6ca71-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6ca71-147">NOTES</span></span>

## <span data-ttu-id="6ca71-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6ca71-148">RELATED LINKS</span></span>
