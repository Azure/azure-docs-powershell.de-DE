---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41defe467244647f707bae16c653dfcbe99eaec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482538"
---
# <span data-ttu-id="4f7a7-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4f7a7-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="4f7a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f7a7-102">SYNOPSIS</span></span>
<span data-ttu-id="4f7a7-103">Erstellt ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f7a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f7a7-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f7a7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f7a7-105">DESCRIPTION</span></span>
<span data-ttu-id="4f7a7-106">Das Cmdlet **New-AzureRmCognitiveServicesAccount** erstellt ein Cognitive Services-Konto mit dem angegebenen Typ und der angegebenen SKU.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="4f7a7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f7a7-107">EXAMPLES</span></span>

### <span data-ttu-id="4f7a7-108">1:</span><span class="sxs-lookup"><span data-stu-id="4f7a7-108">1:</span></span>
```
PS C:\> New-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
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

## <span data-ttu-id="4f7a7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f7a7-109">PARAMETERS</span></span>

### <span data-ttu-id="4f7a7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f7a7-110">-DefaultProfile</span></span>
<span data-ttu-id="4f7a7-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4f7a7-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f7a7-112">-Force</span><span class="sxs-lookup"><span data-stu-id="4f7a7-112">-Force</span></span>
<span data-ttu-id="4f7a7-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4f7a7-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="4f7a7-114">-Location</span></span>
<span data-ttu-id="4f7a7-115">Gibt den Ort an, an dem das Konto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-115">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="4f7a7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4f7a7-116">-Name</span></span>
<span data-ttu-id="4f7a7-117">Gibt den Namen für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-117">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="4f7a7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f7a7-118">-ResourceGroupName</span></span>
<span data-ttu-id="4f7a7-119">Gibt den Namen der Ressourcengruppe an, der das Konto zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="4f7a7-120">Die Ressourcengruppe muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-120">The resource group must already exist.</span></span>

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

### <span data-ttu-id="4f7a7-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4f7a7-121">-SkuName</span></span>
<span data-ttu-id="4f7a7-122">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="4f7a7-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4f7a7-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4f7a7-124">F0 (﻿Kostenlose Ebene)</span><span class="sxs-lookup"><span data-stu-id="4f7a7-124">F0 (free tier)</span></span>
- <span data-ttu-id="4f7a7-125">S0</span><span class="sxs-lookup"><span data-stu-id="4f7a7-125">S0</span></span>
- <span data-ttu-id="4f7a7-126">S1</span><span class="sxs-lookup"><span data-stu-id="4f7a7-126">S1</span></span>
- <span data-ttu-id="4f7a7-127">S2</span><span class="sxs-lookup"><span data-stu-id="4f7a7-127">S2</span></span>
- <span data-ttu-id="4f7a7-128">S3</span><span class="sxs-lookup"><span data-stu-id="4f7a7-128">S3</span></span>
- <span data-ttu-id="4f7a7-129">S4 Weitere Informationen finden Sie unter [kognitive Dienst-APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="4f7a7-129">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="4f7a7-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="4f7a7-130">-Tag</span></span>
<span data-ttu-id="4f7a7-131">Gibt ein Tag als Name-Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-131">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="4f7a7-132">-Typ</span><span class="sxs-lookup"><span data-stu-id="4f7a7-132">-Type</span></span>
<span data-ttu-id="4f7a7-133">Gibt den Typ des zu erstellende Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-133">Specifies the type of account to create.</span></span> <span data-ttu-id="4f7a7-134">Verwenden Sie `Get-AzureRmCognitiveServicesAccountType` das Cmdlet zum Abrufen der aktuellen akzeptablen Werte.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-134">Use `Get-AzureRmCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="4f7a7-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4f7a7-135">-Confirm</span></span>
<span data-ttu-id="4f7a7-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f7a7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f7a7-137">-WhatIf</span></span>
<span data-ttu-id="4f7a7-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f7a7-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f7a7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f7a7-140">CommonParameters</span></span>
<span data-ttu-id="4f7a7-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f7a7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f7a7-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f7a7-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f7a7-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f7a7-143">INPUTS</span></span>

### <span data-ttu-id="4f7a7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4f7a7-144">System.String</span></span>

## <span data-ttu-id="4f7a7-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f7a7-145">OUTPUTS</span></span>

### <span data-ttu-id="4f7a7-146">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4f7a7-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="4f7a7-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f7a7-147">NOTES</span></span>

## <span data-ttu-id="4f7a7-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f7a7-148">RELATED LINKS</span></span>

[<span data-ttu-id="4f7a7-149">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4f7a7-149">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4f7a7-150">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4f7a7-150">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4f7a7-151">Satz-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4f7a7-151">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
