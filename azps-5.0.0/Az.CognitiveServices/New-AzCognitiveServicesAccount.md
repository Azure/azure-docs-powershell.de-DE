---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 0c7e22174b0306a3b9b5a37bd99edeb06f124334
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299667"
---
# <span data-ttu-id="018b0-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="018b0-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="018b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="018b0-102">SYNOPSIS</span></span>
<span data-ttu-id="018b0-103">Erstellt ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="018b0-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="018b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="018b0-104">SYNTAX</span></span>

### <span data-ttu-id="018b0-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="018b0-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="018b0-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="018b0-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="018b0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="018b0-107">DESCRIPTION</span></span>
<span data-ttu-id="018b0-108">Das Cmdlet **New-AzCognitiveServicesAccount** erstellt ein Cognitive Services-Konto mit dem angegebenen Typ und der angegebenen SKU.</span><span class="sxs-lookup"><span data-stu-id="018b0-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="018b0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="018b0-109">EXAMPLES</span></span>

### <span data-ttu-id="018b0-110">1:</span><span class="sxs-lookup"><span data-stu-id="018b0-110">1:</span></span>
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

## <span data-ttu-id="018b0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="018b0-111">PARAMETERS</span></span>

### <span data-ttu-id="018b0-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="018b0-112">-ApiProperty</span></span>
<span data-ttu-id="018b0-113">Die ApiProperties des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="018b0-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="018b0-114">Für bestimmte Kontotypen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="018b0-114">Required by specific account types.</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="018b0-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="018b0-115">-AssignIdentity</span></span>
<span data-ttu-id="018b0-116">Generieren und Zuweisen einer neuen kognitiven Dienstkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="018b0-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="018b0-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="018b0-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="018b0-118">Gibt an, ob die Schlüsselquelle für die kognitive Dienstkonto Verschlüsselung auf Microsoft. CognitiveServices festgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="018b0-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="018b0-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="018b0-119">-CustomSubdomainName</span></span>
<span data-ttu-id="018b0-120">Name des kognitiven Dienstkonto-untergeordneten Bereichs</span><span class="sxs-lookup"><span data-stu-id="018b0-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="018b0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018b0-121">-DefaultProfile</span></span>
<span data-ttu-id="018b0-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="018b0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="018b0-123">-Force</span><span class="sxs-lookup"><span data-stu-id="018b0-123">-Force</span></span>
<span data-ttu-id="018b0-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="018b0-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="018b0-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="018b0-125">-KeyName</span></span>
<span data-ttu-id="018b0-126">Keyvault-keyvault-keyName für Cognitive Services-Konto Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="018b0-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="018b0-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="018b0-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="018b0-128">Gibt an, ob die Schlüsselquelle für die kognitive Dienstkonto Verschlüsselung auf Microsoft. keyvault festgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="018b0-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="018b0-129">Wenn Sie keyName, keyversion und KeyVaultUri angeben, wird die Schlüsselquelle für das kognitive Dienstkonto auch auf Microsoft festgelegt. keyvault-Wetter dieser Parameter ist festgelegt oder nicht.</span><span class="sxs-lookup"><span data-stu-id="018b0-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="018b0-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="018b0-130">-KeyVaultUri</span></span>
<span data-ttu-id="018b0-131">Kognitive Dienstkonto Verschlüsselung keyvault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="018b0-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="018b0-132">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="018b0-132">-KeyVersion</span></span>
<span data-ttu-id="018b0-133">Keyvault-keyvault-Schlüssel Version für kognitive Dienstkonten Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="018b0-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="018b0-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="018b0-134">-Location</span></span>
<span data-ttu-id="018b0-135">Gibt den Ort an, an dem das Konto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="018b0-135">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="018b0-136">-Name</span><span class="sxs-lookup"><span data-stu-id="018b0-136">-Name</span></span>
<span data-ttu-id="018b0-137">Gibt den Namen für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="018b0-137">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="018b0-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="018b0-138">-NetworkRuleSet</span></span>
<span data-ttu-id="018b0-139">NetworkRuleSet wird verwendet, um eine Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke zu definieren sowie Werte für Netzwerkeigenschaften festzulegen, beispielsweise zum Behandeln von Anforderungen, die keiner der definierten Regeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="018b0-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="018b0-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="018b0-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="018b0-141">Der Netzwerkzugriffstyp für das Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="018b0-141">The network access type for Cognitive Services Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="018b0-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="018b0-142">-ResourceGroupName</span></span>
<span data-ttu-id="018b0-143">Gibt den Namen der Ressourcengruppe an, der das Konto zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="018b0-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="018b0-144">Die Ressourcengruppe muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="018b0-144">The resource group must already exist.</span></span>

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

### <span data-ttu-id="018b0-145">-SkuName</span><span class="sxs-lookup"><span data-stu-id="018b0-145">-SkuName</span></span>
<span data-ttu-id="018b0-146">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="018b0-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="018b0-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="018b0-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="018b0-148">F0 (﻿Kostenlose Ebene)</span><span class="sxs-lookup"><span data-stu-id="018b0-148">F0 (free tier)</span></span>
- <span data-ttu-id="018b0-149">S0</span><span class="sxs-lookup"><span data-stu-id="018b0-149">S0</span></span>
- <span data-ttu-id="018b0-150">S1</span><span class="sxs-lookup"><span data-stu-id="018b0-150">S1</span></span>
- <span data-ttu-id="018b0-151">S2</span><span class="sxs-lookup"><span data-stu-id="018b0-151">S2</span></span>
- <span data-ttu-id="018b0-152">S3</span><span class="sxs-lookup"><span data-stu-id="018b0-152">S3</span></span>
- <span data-ttu-id="018b0-153">S4 Weitere Informationen finden Sie unter [kognitive Dienst-APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="018b0-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="018b0-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="018b0-154">-StorageAccountId</span></span>
<span data-ttu-id="018b0-155">Liste der benutzereigenen Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="018b0-155">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="018b0-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="018b0-156">-Tag</span></span>
<span data-ttu-id="018b0-157">Gibt ein Tag als Name-Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="018b0-157">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="018b0-158">-Typ</span><span class="sxs-lookup"><span data-stu-id="018b0-158">-Type</span></span>
<span data-ttu-id="018b0-159">Gibt den Typ des zu erstellende Kontos an.</span><span class="sxs-lookup"><span data-stu-id="018b0-159">Specifies the type of account to create.</span></span> <span data-ttu-id="018b0-160">Verwenden Sie `Get-AzCognitiveServicesAccountType` das Cmdlet zum Abrufen der aktuellen akzeptablen Werte.</span><span class="sxs-lookup"><span data-stu-id="018b0-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="018b0-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="018b0-161">-Confirm</span></span>
<span data-ttu-id="018b0-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="018b0-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="018b0-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="018b0-163">-WhatIf</span></span>
<span data-ttu-id="018b0-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="018b0-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="018b0-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="018b0-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="018b0-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018b0-166">CommonParameters</span></span>
<span data-ttu-id="018b0-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="018b0-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018b0-168">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="018b0-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018b0-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="018b0-169">INPUTS</span></span>

### <span data-ttu-id="018b0-170">System. String</span><span class="sxs-lookup"><span data-stu-id="018b0-170">System.String</span></span>

## <span data-ttu-id="018b0-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="018b0-171">OUTPUTS</span></span>

### <span data-ttu-id="018b0-172">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="018b0-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="018b0-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="018b0-173">NOTES</span></span>

## <span data-ttu-id="018b0-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="018b0-174">RELATED LINKS</span></span>

[<span data-ttu-id="018b0-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="018b0-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="018b0-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="018b0-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="018b0-177">Satz-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="018b0-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
