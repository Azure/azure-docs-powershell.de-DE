---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846327"
---
# <span data-ttu-id="a4736-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="a4736-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="a4736-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4736-102">SYNOPSIS</span></span>
<span data-ttu-id="a4736-103">Erstellt ein Profilobjekt für den Support Kontakt.</span><span class="sxs-lookup"><span data-stu-id="a4736-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="a4736-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4736-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4736-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4736-105">DESCRIPTION</span></span>
<span data-ttu-id="a4736-106">Hierbei handelt es sich um ein Hilfsprogramm-Cmdlet, mit dem Sie beim Erstellen oder Aktualisieren eines Support Tickets ein Support-Kontakt Profilobjekt erstellen können.</span><span class="sxs-lookup"><span data-stu-id="a4736-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="a4736-107">Sie müssen die folgenden Parameter angeben, die für das Erstellen eines Support Tickets obligatorisch sind:</span><span class="sxs-lookup"><span data-stu-id="a4736-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="a4736-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4736-108">EXAMPLES</span></span>

### <span data-ttu-id="a4736-109">Beispiel 1: Erstellen eines Kontaktobjekts</span><span class="sxs-lookup"><span data-stu-id="a4736-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="a4736-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4736-110">PARAMETERS</span></span>

### <span data-ttu-id="a4736-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a4736-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="a4736-112">Die hier aufgelisteten e-Mail-Adressen werden auf jede Korrespondenz über das Support-Ticket kopiert.</span><span class="sxs-lookup"><span data-stu-id="a4736-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="a4736-113">-Land</span><span class="sxs-lookup"><span data-stu-id="a4736-113">-Country</span></span>
<span data-ttu-id="a4736-114">Kunden Land.</span><span class="sxs-lookup"><span data-stu-id="a4736-114">Customer country.</span></span>
<span data-ttu-id="a4736-115">Dies muss eine gültige ISO-Alpha-3-Landesvorwahl (ISO 3166) sein.</span><span class="sxs-lookup"><span data-stu-id="a4736-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="a4736-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4736-116">-DefaultProfile</span></span>
<span data-ttu-id="a4736-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4736-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4736-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="a4736-118">-FirstName</span></span>
<span data-ttu-id="a4736-119">Name des Kunden Vornamens</span><span class="sxs-lookup"><span data-stu-id="a4736-119">Customer first name.</span></span>

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

### <span data-ttu-id="a4736-120">-Nachname</span><span class="sxs-lookup"><span data-stu-id="a4736-120">-LastName</span></span>
<span data-ttu-id="a4736-121">Nachname des Kunden</span><span class="sxs-lookup"><span data-stu-id="a4736-121">Customer last name.</span></span>

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

### <span data-ttu-id="a4736-122">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="a4736-122">-PhoneNumber</span></span>
<span data-ttu-id="a4736-123">Kundentelefonnummer.</span><span class="sxs-lookup"><span data-stu-id="a4736-123">Customer phone number.</span></span>
<span data-ttu-id="a4736-124">Dies ist erforderlich, wenn die bevorzugte Kontaktmethode Telefon ist.</span><span class="sxs-lookup"><span data-stu-id="a4736-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="a4736-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="a4736-125">-PreferredContactMethod</span></span>
<span data-ttu-id="a4736-126">Bevorzugte Kontaktmethode.</span><span class="sxs-lookup"><span data-stu-id="a4736-126">Preferred contact method.</span></span>

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

### <span data-ttu-id="a4736-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="a4736-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="a4736-128">Kunden bevorzugte Support Sprache.</span><span class="sxs-lookup"><span data-stu-id="a4736-128">Customer preferred support language.</span></span>
<span data-ttu-id="a4736-129">Hierbei muss es sich um einen gültigen sprach Fortsetzungs Code für eine der hier aufgeführten unterstützten Sprachen handeln https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="a4736-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="a4736-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="a4736-130">-PreferredTimeZone</span></span>
<span data-ttu-id="a4736-131">Bevorzugte Zeitzone des Kunden.</span><span class="sxs-lookup"><span data-stu-id="a4736-131">Customer preferred time zone.</span></span>
<span data-ttu-id="a4736-132">Dies muss ein gültiger System.TimeZoneInfo.ID-Wert sein.</span><span class="sxs-lookup"><span data-stu-id="a4736-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="a4736-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a4736-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="a4736-134">Primäre e-Mail-Adresse des Kunden.</span><span class="sxs-lookup"><span data-stu-id="a4736-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="a4736-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a4736-135">-Confirm</span></span>
<span data-ttu-id="a4736-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a4736-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4736-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4736-137">-WhatIf</span></span>
<span data-ttu-id="a4736-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4736-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4736-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4736-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4736-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4736-140">CommonParameters</span></span>
<span data-ttu-id="a4736-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4736-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4736-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4736-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4736-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4736-143">INPUTS</span></span>

### <span data-ttu-id="a4736-144">Keine</span><span class="sxs-lookup"><span data-stu-id="a4736-144">None</span></span>

## <span data-ttu-id="a4736-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4736-145">OUTPUTS</span></span>

### <span data-ttu-id="a4736-146">Microsoft. Azure. Commands. Support. Models. PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="a4736-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="a4736-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4736-147">NOTES</span></span>

## <span data-ttu-id="a4736-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4736-148">RELATED LINKS</span></span>
