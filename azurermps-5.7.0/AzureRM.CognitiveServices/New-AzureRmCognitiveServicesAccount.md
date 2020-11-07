---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 1c1d4ad776ed3db2cb3b5adfb490902a7de12f42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662374"
---
# <span data-ttu-id="9e87a-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9e87a-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="9e87a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e87a-102">SYNOPSIS</span></span>
<span data-ttu-id="9e87a-103">Erstellt ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="9e87a-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e87a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e87a-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e87a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e87a-105">DESCRIPTION</span></span>
<span data-ttu-id="9e87a-106">Das Cmdlet **New-AzureRmCognitiveServicesAccount** erstellt ein Cognitive Services-Konto mit dem angegebenen Typ und der angegebenen SKU.</span><span class="sxs-lookup"><span data-stu-id="9e87a-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="9e87a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e87a-107">EXAMPLES</span></span>

### <span data-ttu-id="9e87a-108">1:</span><span class="sxs-lookup"><span data-stu-id="9e87a-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="9e87a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e87a-109">PARAMETERS</span></span>

### <span data-ttu-id="9e87a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e87a-110">-DefaultProfile</span></span>
<span data-ttu-id="9e87a-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9e87a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e87a-112">-Force</span><span class="sxs-lookup"><span data-stu-id="9e87a-112">-Force</span></span>
<span data-ttu-id="9e87a-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9e87a-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e87a-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="9e87a-114">-Location</span></span>
<span data-ttu-id="9e87a-115">Gibt den Ort an, an dem das Konto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e87a-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e87a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9e87a-116">-Name</span></span>
<span data-ttu-id="9e87a-117">Gibt den Namen für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="9e87a-117">Specifies the name for the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e87a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e87a-118">-ResourceGroupName</span></span>
<span data-ttu-id="9e87a-119">Gibt den Namen der Ressourcengruppe an, der das Konto zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e87a-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="9e87a-120">Die Ressourcengruppe muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="9e87a-120">The resource group must already exist.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e87a-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9e87a-121">-SkuName</span></span>
<span data-ttu-id="9e87a-122">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="9e87a-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="9e87a-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9e87a-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e87a-124">F0 (﻿Kostenlose Ebene)</span><span class="sxs-lookup"><span data-stu-id="9e87a-124">F0 (free tier)</span></span>
- <span data-ttu-id="9e87a-125">S0</span><span class="sxs-lookup"><span data-stu-id="9e87a-125">S0</span></span>
- <span data-ttu-id="9e87a-126">S1</span><span class="sxs-lookup"><span data-stu-id="9e87a-126">S1</span></span>
- <span data-ttu-id="9e87a-127">S2</span><span class="sxs-lookup"><span data-stu-id="9e87a-127">S2</span></span>
- <span data-ttu-id="9e87a-128">S3</span><span class="sxs-lookup"><span data-stu-id="9e87a-128">S3</span></span>
- <span data-ttu-id="9e87a-129">S4</span><span class="sxs-lookup"><span data-stu-id="9e87a-129">S4</span></span>

<span data-ttu-id="9e87a-130">Weitere Informationen finden Sie unter [kognitive Dienst-APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="9e87a-130">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e87a-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e87a-131">-Tag</span></span>
<span data-ttu-id="9e87a-132">Gibt ein Tag als Name-Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="9e87a-132">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e87a-133">-Typ</span><span class="sxs-lookup"><span data-stu-id="9e87a-133">-Type</span></span>
<span data-ttu-id="9e87a-134">Gibt den Typ des zu erstellende Kontos an.</span><span class="sxs-lookup"><span data-stu-id="9e87a-134">Specifies the type of account to create.</span></span> <span data-ttu-id="9e87a-135">Aktuelle zulässige Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="9e87a-135">Current acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e87a-136">Bing. AutoSuggest. V7</span><span class="sxs-lookup"><span data-stu-id="9e87a-136">Bing.Autosuggest.v7</span></span>
- <span data-ttu-id="9e87a-137">Bing. CustomSearch</span><span class="sxs-lookup"><span data-stu-id="9e87a-137">Bing.CustomSearch</span></span>
- <span data-ttu-id="9e87a-138">Bing. search. V7</span><span class="sxs-lookup"><span data-stu-id="9e87a-138">Bing.Search.v7</span></span>
- <span data-ttu-id="9e87a-139">Bing. Speech</span><span class="sxs-lookup"><span data-stu-id="9e87a-139">Bing.Speech</span></span>
- <span data-ttu-id="9e87a-140">Bing. SpellCheck. V7</span><span class="sxs-lookup"><span data-stu-id="9e87a-140">Bing.SpellCheck.v7</span></span>
- <span data-ttu-id="9e87a-141">Computer Vision</span><span class="sxs-lookup"><span data-stu-id="9e87a-141">ComputerVision</span></span>
- <span data-ttu-id="9e87a-142">ContentModerator</span><span class="sxs-lookup"><span data-stu-id="9e87a-142">ContentModerator</span></span>
- <span data-ttu-id="9e87a-143">CustomSpeech</span><span class="sxs-lookup"><span data-stu-id="9e87a-143">CustomSpeech</span></span>
- <span data-ttu-id="9e87a-144">CustomVision. Prediction</span><span class="sxs-lookup"><span data-stu-id="9e87a-144">CustomVision.Prediction</span></span>
- <span data-ttu-id="9e87a-145">CustomVision. Schulung</span><span class="sxs-lookup"><span data-stu-id="9e87a-145">CustomVision.Training</span></span>
- <span data-ttu-id="9e87a-146">Emotion</span><span class="sxs-lookup"><span data-stu-id="9e87a-146">Emotion</span></span>
- <span data-ttu-id="9e87a-147">Gesicht</span><span class="sxs-lookup"><span data-stu-id="9e87a-147">Face</span></span>
- <span data-ttu-id="9e87a-148">Luis</span><span class="sxs-lookup"><span data-stu-id="9e87a-148">LUIS</span></span>
- <span data-ttu-id="9e87a-149">QnAMaker</span><span class="sxs-lookup"><span data-stu-id="9e87a-149">QnAMaker</span></span>
- <span data-ttu-id="9e87a-150">SpeakerRecognition</span><span class="sxs-lookup"><span data-stu-id="9e87a-150">SpeakerRecognition</span></span>
- <span data-ttu-id="9e87a-151">SpeechTranslation</span><span class="sxs-lookup"><span data-stu-id="9e87a-151">SpeechTranslation</span></span>
- <span data-ttu-id="9e87a-152">Textanalytics</span><span class="sxs-lookup"><span data-stu-id="9e87a-152">TextAnalytics</span></span>
- <span data-ttu-id="9e87a-153">Text Übersetzung</span><span class="sxs-lookup"><span data-stu-id="9e87a-153">TextTranslation</span></span>
- <span data-ttu-id="9e87a-154">WebLM</span><span class="sxs-lookup"><span data-stu-id="9e87a-154">WebLM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e87a-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e87a-155">-Confirm</span></span>
<span data-ttu-id="9e87a-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e87a-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e87a-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e87a-157">-WhatIf</span></span>
<span data-ttu-id="9e87a-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e87a-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e87a-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e87a-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e87a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e87a-160">CommonParameters</span></span>
<span data-ttu-id="9e87a-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e87a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e87a-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e87a-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e87a-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e87a-163">INPUTS</span></span>

### <span data-ttu-id="9e87a-164">Keine</span><span class="sxs-lookup"><span data-stu-id="9e87a-164">None</span></span>
<span data-ttu-id="9e87a-165">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9e87a-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e87a-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e87a-166">OUTPUTS</span></span>

### <span data-ttu-id="9e87a-167">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9e87a-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="9e87a-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e87a-168">NOTES</span></span>

## <span data-ttu-id="9e87a-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e87a-169">RELATED LINKS</span></span>

[<span data-ttu-id="9e87a-170">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9e87a-170">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="9e87a-171">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9e87a-171">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="9e87a-172">Satz-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9e87a-172">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
