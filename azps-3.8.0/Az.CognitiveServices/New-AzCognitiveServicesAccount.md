---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 713c5cb34133a233bace576ea80035b8e004eb7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995015"
---
# <span data-ttu-id="453be-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="453be-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="453be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="453be-102">SYNOPSIS</span></span>
<span data-ttu-id="453be-103">Erstellt ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="453be-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="453be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="453be-104">SYNTAX</span></span>

### <span data-ttu-id="453be-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="453be-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="453be-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="453be-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="453be-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="453be-107">DESCRIPTION</span></span>
<span data-ttu-id="453be-108">Das Cmdlet **New-AzCognitiveServicesAccount** erstellt ein Cognitive Services-Konto mit dem angegebenen Typ und der angegebenen SKU.</span><span class="sxs-lookup"><span data-stu-id="453be-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="453be-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="453be-109">EXAMPLES</span></span>

### <span data-ttu-id="453be-110">1:</span><span class="sxs-lookup"><span data-stu-id="453be-110">1:</span></span>
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

## <span data-ttu-id="453be-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="453be-111">PARAMETERS</span></span>

### <span data-ttu-id="453be-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="453be-112">-AssignIdentity</span></span>
<span data-ttu-id="453be-113">Generieren und Zuweisen einer neuen kognitiven Dienstkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="453be-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="453be-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="453be-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="453be-115">Gibt an, ob die Schlüsselquelle für die kognitive Dienstkonto Verschlüsselung auf Microsoft. CognitiveServices festgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="453be-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CognitiveServicesEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453be-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="453be-116">-CustomSubdomainName</span></span>
<span data-ttu-id="453be-117">Name des kognitiven Dienstkonto-untergeordneten Bereichs</span><span class="sxs-lookup"><span data-stu-id="453be-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="453be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="453be-118">-DefaultProfile</span></span>
<span data-ttu-id="453be-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="453be-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="453be-120">-Force</span><span class="sxs-lookup"><span data-stu-id="453be-120">-Force</span></span>
<span data-ttu-id="453be-121">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="453be-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="453be-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="453be-122">-KeyName</span></span>
<span data-ttu-id="453be-123">Keyvault-keyvault-keyName für Cognitive Services-Konto Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="453be-123">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453be-124">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="453be-124">-KeyVaultEncryption</span></span>
<span data-ttu-id="453be-125">Gibt an, ob die Schlüsselquelle für die kognitive Dienstkonto Verschlüsselung auf Microsoft. keyvault festgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="453be-125">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="453be-126">Wenn Sie keyName, keyversion und KeyVaultUri angeben, wird die Schlüsselquelle für das kognitive Dienstkonto auch auf Microsoft festgelegt. keyvault-Wetter dieser Parameter ist festgelegt oder nicht.</span><span class="sxs-lookup"><span data-stu-id="453be-126">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyVaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453be-127">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="453be-127">-KeyVaultUri</span></span>
<span data-ttu-id="453be-128">Kognitive Dienstkonto Verschlüsselung keyvault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="453be-128">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453be-129">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="453be-129">-KeyVersion</span></span>
<span data-ttu-id="453be-130">Keyvault-keyvault-Schlüssel Version für kognitive Dienstkonten Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="453be-130">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453be-131">-Standort</span><span class="sxs-lookup"><span data-stu-id="453be-131">-Location</span></span>
<span data-ttu-id="453be-132">Gibt den Ort an, an dem das Konto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="453be-132">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="453be-133">-Name</span><span class="sxs-lookup"><span data-stu-id="453be-133">-Name</span></span>
<span data-ttu-id="453be-134">Gibt den Namen für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="453be-134">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="453be-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="453be-135">-NetworkRuleSet</span></span>
<span data-ttu-id="453be-136">NetworkRuleSet wird verwendet, um eine Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke zu definieren sowie Werte für Netzwerkeigenschaften festzulegen, beispielsweise zum Behandeln von Anforderungen, die keiner der definierten Regeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="453be-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453be-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="453be-137">-ResourceGroupName</span></span>
<span data-ttu-id="453be-138">Gibt den Namen der Ressourcengruppe an, der das Konto zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="453be-138">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="453be-139">Die Ressourcengruppe muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="453be-139">The resource group must already exist.</span></span>

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

### <span data-ttu-id="453be-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="453be-140">-SkuName</span></span>
<span data-ttu-id="453be-141">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="453be-141">Specifies the SKU for the account.</span></span>
<span data-ttu-id="453be-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="453be-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="453be-143">F0 (﻿Kostenlose Ebene)</span><span class="sxs-lookup"><span data-stu-id="453be-143">F0 (free tier)</span></span>
- <span data-ttu-id="453be-144">S0</span><span class="sxs-lookup"><span data-stu-id="453be-144">S0</span></span>
- <span data-ttu-id="453be-145">S1</span><span class="sxs-lookup"><span data-stu-id="453be-145">S1</span></span>
- <span data-ttu-id="453be-146">S2</span><span class="sxs-lookup"><span data-stu-id="453be-146">S2</span></span>
- <span data-ttu-id="453be-147">S3</span><span class="sxs-lookup"><span data-stu-id="453be-147">S3</span></span>
- <span data-ttu-id="453be-148">S4 Weitere Informationen finden Sie unter [kognitive Dienst-APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="453be-148">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="453be-149">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="453be-149">-StorageAccountId</span></span>
<span data-ttu-id="453be-150">Liste der benutzereigenen Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="453be-150">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="453be-151">-Tag</span><span class="sxs-lookup"><span data-stu-id="453be-151">-Tag</span></span>
<span data-ttu-id="453be-152">Gibt ein Tag als Name-Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="453be-152">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="453be-153">-Typ</span><span class="sxs-lookup"><span data-stu-id="453be-153">-Type</span></span>
<span data-ttu-id="453be-154">Gibt den Typ des zu erstellende Kontos an.</span><span class="sxs-lookup"><span data-stu-id="453be-154">Specifies the type of account to create.</span></span> <span data-ttu-id="453be-155">Verwenden Sie `Get-AzCognitiveServicesAccountType` das Cmdlet zum Abrufen der aktuellen akzeptablen Werte.</span><span class="sxs-lookup"><span data-stu-id="453be-155">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="453be-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="453be-156">-Confirm</span></span>
<span data-ttu-id="453be-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="453be-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="453be-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="453be-158">-WhatIf</span></span>
<span data-ttu-id="453be-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="453be-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="453be-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="453be-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="453be-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="453be-161">CommonParameters</span></span>
<span data-ttu-id="453be-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="453be-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="453be-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="453be-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="453be-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="453be-164">INPUTS</span></span>

### <span data-ttu-id="453be-165">System. String</span><span class="sxs-lookup"><span data-stu-id="453be-165">System.String</span></span>

## <span data-ttu-id="453be-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="453be-166">OUTPUTS</span></span>

### <span data-ttu-id="453be-167">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="453be-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="453be-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="453be-168">NOTES</span></span>

## <span data-ttu-id="453be-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="453be-169">RELATED LINKS</span></span>

[<span data-ttu-id="453be-170">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="453be-170">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="453be-171">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="453be-171">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="453be-172">Satz-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="453be-172">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
