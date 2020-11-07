---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 7e5253951ec3c74850584aaac9818a6a7c8f2737
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661595"
---
# <span data-ttu-id="ed79b-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ed79b-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="ed79b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed79b-102">SYNOPSIS</span></span>
<span data-ttu-id="ed79b-103">Erstellt ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="ed79b-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="ed79b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed79b-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed79b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed79b-105">DESCRIPTION</span></span>
<span data-ttu-id="ed79b-106">Das Cmdlet **New-AzCognitiveServicesAccount** erstellt ein Cognitive Services-Konto mit dem angegebenen Typ und der angegebenen SKU.</span><span class="sxs-lookup"><span data-stu-id="ed79b-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="ed79b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed79b-107">EXAMPLES</span></span>

### <span data-ttu-id="ed79b-108">1:</span><span class="sxs-lookup"><span data-stu-id="ed79b-108">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="ed79b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed79b-109">PARAMETERS</span></span>

### <span data-ttu-id="ed79b-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="ed79b-110">-CustomSubdomainName</span></span>
<span data-ttu-id="ed79b-111">Name des kognitiven Dienstkonto-untergeordneten Bereichs</span><span class="sxs-lookup"><span data-stu-id="ed79b-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="ed79b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed79b-112">-DefaultProfile</span></span>
<span data-ttu-id="ed79b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ed79b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed79b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ed79b-114">-Force</span></span>
<span data-ttu-id="ed79b-115">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ed79b-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed79b-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="ed79b-116">-Location</span></span>
<span data-ttu-id="ed79b-117">Gibt den Ort an, an dem das Konto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed79b-117">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed79b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ed79b-118">-Name</span></span>
<span data-ttu-id="ed79b-119">Gibt den Namen für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="ed79b-119">Specifies the name for the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed79b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed79b-120">-ResourceGroupName</span></span>
<span data-ttu-id="ed79b-121">Gibt den Namen der Ressourcengruppe an, der das Konto zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed79b-121">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="ed79b-122">Die Ressourcengruppe muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ed79b-122">The resource group must already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed79b-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ed79b-123">-SkuName</span></span>
<span data-ttu-id="ed79b-124">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="ed79b-124">Specifies the SKU for the account.</span></span>
<span data-ttu-id="ed79b-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ed79b-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed79b-126">F0 (﻿Kostenlose Ebene)</span><span class="sxs-lookup"><span data-stu-id="ed79b-126">F0 (free tier)</span></span>
- <span data-ttu-id="ed79b-127">S0</span><span class="sxs-lookup"><span data-stu-id="ed79b-127">S0</span></span>
- <span data-ttu-id="ed79b-128">S1</span><span class="sxs-lookup"><span data-stu-id="ed79b-128">S1</span></span>
- <span data-ttu-id="ed79b-129">S2</span><span class="sxs-lookup"><span data-stu-id="ed79b-129">S2</span></span>
- <span data-ttu-id="ed79b-130">S3</span><span class="sxs-lookup"><span data-stu-id="ed79b-130">S3</span></span>
- <span data-ttu-id="ed79b-131">S4 Weitere Informationen finden Sie unter [kognitive Dienst-APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="ed79b-131">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed79b-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed79b-132">-Tag</span></span>
<span data-ttu-id="ed79b-133">Gibt ein Tag als Name-Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="ed79b-133">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed79b-134">-Typ</span><span class="sxs-lookup"><span data-stu-id="ed79b-134">-Type</span></span>
<span data-ttu-id="ed79b-135">Gibt den Typ des zu erstellende Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ed79b-135">Specifies the type of account to create.</span></span> <span data-ttu-id="ed79b-136">Verwenden Sie `Get-AzCognitiveServicesAccountType` das Cmdlet zum Abrufen der aktuellen akzeptablen Werte.</span><span class="sxs-lookup"><span data-stu-id="ed79b-136">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed79b-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed79b-137">-Confirm</span></span>
<span data-ttu-id="ed79b-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed79b-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed79b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed79b-139">-WhatIf</span></span>
<span data-ttu-id="ed79b-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed79b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed79b-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed79b-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed79b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed79b-142">CommonParameters</span></span>
<span data-ttu-id="ed79b-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed79b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed79b-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed79b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed79b-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed79b-145">INPUTS</span></span>

### <span data-ttu-id="ed79b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ed79b-146">System.String</span></span>

## <span data-ttu-id="ed79b-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed79b-147">OUTPUTS</span></span>

### <span data-ttu-id="ed79b-148">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ed79b-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="ed79b-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed79b-149">NOTES</span></span>

## <span data-ttu-id="ed79b-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed79b-150">RELATED LINKS</span></span>

[<span data-ttu-id="ed79b-151">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ed79b-151">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="ed79b-152">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ed79b-152">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="ed79b-153">Satz-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ed79b-153">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
