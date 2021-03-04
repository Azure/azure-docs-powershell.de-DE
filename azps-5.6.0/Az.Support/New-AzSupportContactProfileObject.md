---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 5b2dfbc472b128a12f108aafc92aa9d30b661255
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944398"
---
# <span data-ttu-id="3ba93-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="3ba93-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="3ba93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ba93-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba93-103">Erstellt ein Supportkontaktprofilobjekt.</span><span class="sxs-lookup"><span data-stu-id="3ba93-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="3ba93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ba93-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ba93-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ba93-105">DESCRIPTION</span></span>
<span data-ttu-id="3ba93-106">Dies ist ein Hilfs-Cmdlet, das Sie zum Erstellen eines Supportkontaktprofilobjekts verwenden können, wenn Sie ein Supportticket erstellen oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3ba93-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="3ba93-107">Sie müssen die folgenden Parameter angeben, die für die Erstellung eines Supporttickets obligatorisch sind:</span><span class="sxs-lookup"><span data-stu-id="3ba93-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="3ba93-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ba93-108">EXAMPLES</span></span>

### <span data-ttu-id="3ba93-109">Beispiel 1: Erstellen eines Kontaktobjekts</span><span class="sxs-lookup"><span data-stu-id="3ba93-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="3ba93-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3ba93-110">PARAMETERS</span></span>

### <span data-ttu-id="3ba93-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3ba93-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="3ba93-112">Die hier aufgeführten E-Mail-Adressen werden in jede Korrespondenz über das Supportticket kopiert.</span><span class="sxs-lookup"><span data-stu-id="3ba93-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="3ba93-113">-Land</span><span class="sxs-lookup"><span data-stu-id="3ba93-113">-Country</span></span>
<span data-ttu-id="3ba93-114">Kundenland.</span><span class="sxs-lookup"><span data-stu-id="3ba93-114">Customer country.</span></span>
<span data-ttu-id="3ba93-115">Dies muss ein gültiger ISO Alpha-3-Ländercode (ISO 3166) sein.</span><span class="sxs-lookup"><span data-stu-id="3ba93-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="3ba93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba93-116">-DefaultProfile</span></span>
<span data-ttu-id="3ba93-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ba93-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ba93-118">-Vorname</span><span class="sxs-lookup"><span data-stu-id="3ba93-118">-FirstName</span></span>
<span data-ttu-id="3ba93-119">Vorname des Kunden.</span><span class="sxs-lookup"><span data-stu-id="3ba93-119">Customer first name.</span></span>

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

### <span data-ttu-id="3ba93-120">-Nachname</span><span class="sxs-lookup"><span data-stu-id="3ba93-120">-LastName</span></span>
<span data-ttu-id="3ba93-121">Nachname des Kunden.</span><span class="sxs-lookup"><span data-stu-id="3ba93-121">Customer last name.</span></span>

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

### <span data-ttu-id="3ba93-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="3ba93-122">-PhoneNumber</span></span>
<span data-ttu-id="3ba93-123">Telefonnummer des Kunden.</span><span class="sxs-lookup"><span data-stu-id="3ba93-123">Customer phone number.</span></span>
<span data-ttu-id="3ba93-124">Dies ist erforderlich, wenn die bevorzugte Kontaktmethode das Telefon ist.</span><span class="sxs-lookup"><span data-stu-id="3ba93-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="3ba93-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="3ba93-125">-PreferredContactMethod</span></span>
<span data-ttu-id="3ba93-126">Bevorzugte Kontaktmethode.</span><span class="sxs-lookup"><span data-stu-id="3ba93-126">Preferred contact method.</span></span>

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

### <span data-ttu-id="3ba93-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="3ba93-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="3ba93-128">Bevorzugte Supportsprache des Kunden.</span><span class="sxs-lookup"><span data-stu-id="3ba93-128">Customer preferred support language.</span></span>
<span data-ttu-id="3ba93-129">Dies muss ein gültiger Sprachcode für eine der hier aufgeführten unterstützten Sprachen https://azure.microsoft.com/support/faq/ sein.</span><span class="sxs-lookup"><span data-stu-id="3ba93-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="3ba93-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="3ba93-130">-PreferredTimeZone</span></span>
<span data-ttu-id="3ba93-131">Vom Kunden bevorzugte Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="3ba93-131">Customer preferred time zone.</span></span>
<span data-ttu-id="3ba93-132">Dies muss ein gültiger System.TimeZoneInfo.Id sein.</span><span class="sxs-lookup"><span data-stu-id="3ba93-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="3ba93-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3ba93-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="3ba93-134">Primäre E-Mail-Adresse des Kunden.</span><span class="sxs-lookup"><span data-stu-id="3ba93-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="3ba93-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3ba93-135">-Confirm</span></span>
<span data-ttu-id="3ba93-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ba93-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ba93-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ba93-137">-WhatIf</span></span>
<span data-ttu-id="3ba93-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ba93-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ba93-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ba93-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ba93-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba93-140">CommonParameters</span></span>
<span data-ttu-id="3ba93-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ba93-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba93-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ba93-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba93-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ba93-143">INPUTS</span></span>

### <span data-ttu-id="3ba93-144">Keine</span><span class="sxs-lookup"><span data-stu-id="3ba93-144">None</span></span>

## <span data-ttu-id="3ba93-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ba93-145">OUTPUTS</span></span>

### <span data-ttu-id="3ba93-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="3ba93-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="3ba93-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3ba93-147">NOTES</span></span>

## <span data-ttu-id="3ba93-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3ba93-148">RELATED LINKS</span></span>
