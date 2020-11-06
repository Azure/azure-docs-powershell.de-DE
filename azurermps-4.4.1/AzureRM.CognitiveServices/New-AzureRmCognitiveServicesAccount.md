---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 449b10f851dbd4e2f2e804bab0772543d512c0c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505237"
---
# <span data-ttu-id="58b20-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="58b20-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="58b20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="58b20-102">SYNOPSIS</span></span>
<span data-ttu-id="58b20-103">Erstellt ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="58b20-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58b20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="58b20-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58b20-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58b20-105">DESCRIPTION</span></span>
<span data-ttu-id="58b20-106">Das Cmdlet **New-AzureRmCognitiveServicesAccount** erstellt ein Cognitive Services-Konto mit dem angegebenen Typ und der angegebenen SKU.</span><span class="sxs-lookup"><span data-stu-id="58b20-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="58b20-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58b20-107">EXAMPLES</span></span>

### <span data-ttu-id="58b20-108">1:</span><span class="sxs-lookup"><span data-stu-id="58b20-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="58b20-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="58b20-109">PARAMETERS</span></span>

### <span data-ttu-id="58b20-110">-Force</span><span class="sxs-lookup"><span data-stu-id="58b20-110">-Force</span></span>
<span data-ttu-id="58b20-111">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="58b20-111">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="58b20-112">-Standort</span><span class="sxs-lookup"><span data-stu-id="58b20-112">-Location</span></span>
<span data-ttu-id="58b20-113">Gibt den Ort an, an dem das Konto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="58b20-113">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="58b20-114">-Name</span><span class="sxs-lookup"><span data-stu-id="58b20-114">-Name</span></span>
<span data-ttu-id="58b20-115">Gibt den Namen für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="58b20-115">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="58b20-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58b20-116">-ResourceGroupName</span></span>
<span data-ttu-id="58b20-117">Gibt den Namen der Ressourcengruppe an, der das Konto zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="58b20-117">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="58b20-118">Die Ressourcengruppe muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="58b20-118">The resource group must already exist.</span></span>

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

### <span data-ttu-id="58b20-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="58b20-119">-SkuName</span></span>
<span data-ttu-id="58b20-120">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="58b20-120">Specifies the SKU for the account.</span></span>
<span data-ttu-id="58b20-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="58b20-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="58b20-122">F0 (﻿Kostenlose Ebene)</span><span class="sxs-lookup"><span data-stu-id="58b20-122">F0 (free tier)</span></span>
- <span data-ttu-id="58b20-123">S0</span><span class="sxs-lookup"><span data-stu-id="58b20-123">S0</span></span>
- <span data-ttu-id="58b20-124">S1</span><span class="sxs-lookup"><span data-stu-id="58b20-124">S1</span></span>
- <span data-ttu-id="58b20-125">S2</span><span class="sxs-lookup"><span data-stu-id="58b20-125">S2</span></span>
- <span data-ttu-id="58b20-126">S3</span><span class="sxs-lookup"><span data-stu-id="58b20-126">S3</span></span>
- <span data-ttu-id="58b20-127">S4</span><span class="sxs-lookup"><span data-stu-id="58b20-127">S4</span></span>

<span data-ttu-id="58b20-128">Weitere Informationen finden Sie unter [kognitive Dienst-APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="58b20-128">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="58b20-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="58b20-129">-Tag</span></span>
<span data-ttu-id="58b20-130">Gibt ein Tag als Name-Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="58b20-130">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="58b20-131">-Typ</span><span class="sxs-lookup"><span data-stu-id="58b20-131">-Type</span></span>
<span data-ttu-id="58b20-132">Gibt den Typ des zu erstellende Kontos an. Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="58b20-132">Specifies the type of account to create.The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="58b20-133">Computer Vision</span><span class="sxs-lookup"><span data-stu-id="58b20-133">ComputerVision</span></span>
- <span data-ttu-id="58b20-134">Emotion</span><span class="sxs-lookup"><span data-stu-id="58b20-134">Emotion</span></span>
- <span data-ttu-id="58b20-135">Gesicht</span><span class="sxs-lookup"><span data-stu-id="58b20-135">Face</span></span>
- <span data-ttu-id="58b20-136">Luis</span><span class="sxs-lookup"><span data-stu-id="58b20-136">LUIS</span></span>
- <span data-ttu-id="58b20-137">Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="58b20-137">Recommendations</span></span>
- <span data-ttu-id="58b20-138">Sprach</span><span class="sxs-lookup"><span data-stu-id="58b20-138">Speech</span></span>
- <span data-ttu-id="58b20-139">Textanalytics</span><span class="sxs-lookup"><span data-stu-id="58b20-139">TextAnalytics</span></span>
- <span data-ttu-id="58b20-140">WebLM</span><span class="sxs-lookup"><span data-stu-id="58b20-140">WebLM</span></span>

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

### <span data-ttu-id="58b20-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="58b20-141">-Confirm</span></span>
<span data-ttu-id="58b20-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58b20-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58b20-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58b20-143">-WhatIf</span></span>
<span data-ttu-id="58b20-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58b20-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58b20-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58b20-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58b20-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b20-146">-DefaultProfile</span></span>
<span data-ttu-id="58b20-147">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="58b20-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58b20-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b20-148">CommonParameters</span></span>
<span data-ttu-id="58b20-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58b20-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b20-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58b20-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b20-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="58b20-151">INPUTS</span></span>

## <span data-ttu-id="58b20-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="58b20-152">OUTPUTS</span></span>

### <span data-ttu-id="58b20-153">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="58b20-153">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="58b20-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="58b20-154">NOTES</span></span>

## <span data-ttu-id="58b20-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="58b20-155">RELATED LINKS</span></span>

[<span data-ttu-id="58b20-156">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="58b20-156">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="58b20-157">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="58b20-157">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="58b20-158">Satz-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="58b20-158">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
