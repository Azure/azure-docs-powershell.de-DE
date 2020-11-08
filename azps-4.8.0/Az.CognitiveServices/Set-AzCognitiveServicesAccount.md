---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 5cfbfa0452fba4d01d2af5aa8e6acc3a141a4426
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165904"
---
# <span data-ttu-id="0b195-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0b195-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="0b195-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b195-102">SYNOPSIS</span></span>
<span data-ttu-id="0b195-103">Ändert ein Konto.</span><span class="sxs-lookup"><span data-stu-id="0b195-103">Modifies an account.</span></span>

## <span data-ttu-id="0b195-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b195-104">SYNTAX</span></span>

### <span data-ttu-id="0b195-105">CognitiveServicesEncryption (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b195-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b195-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="0b195-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b195-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b195-107">DESCRIPTION</span></span>
<span data-ttu-id="0b195-108">Das Cmdlet " **Satz-AzCognitiveServicesAccount** " ändert die SKU oder Tags des angegebenen Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="0b195-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="0b195-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b195-109">EXAMPLES</span></span>

### <span data-ttu-id="0b195-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0b195-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="0b195-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b195-111">PARAMETERS</span></span>

### <span data-ttu-id="0b195-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="0b195-112">-ApiProperty</span></span>
<span data-ttu-id="0b195-113">Die ApiProperties des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="0b195-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="0b195-114">Für bestimmte Kontotypen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0b195-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="0b195-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0b195-115">-AssignIdentity</span></span>
<span data-ttu-id="0b195-116">Generieren und Zuweisen einer neuen kognitiven Dienstkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="0b195-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="0b195-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="0b195-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="0b195-118">Gibt an, ob die Schlüsselquelle für die kognitive Dienstkonto Verschlüsselung auf Microsoft. CognitiveServices festgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b195-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="0b195-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="0b195-119">-CustomSubdomainName</span></span>
<span data-ttu-id="0b195-120">Name des kognitiven Dienstkonto-untergeordneten Bereichs</span><span class="sxs-lookup"><span data-stu-id="0b195-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="0b195-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b195-121">-DefaultProfile</span></span>
<span data-ttu-id="0b195-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0b195-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b195-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0b195-123">-Force</span></span>
<span data-ttu-id="0b195-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="0b195-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0b195-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="0b195-125">-IdentityType</span></span>
<span data-ttu-id="0b195-126">Der Typ der verwalteten Dienstidentität.</span><span class="sxs-lookup"><span data-stu-id="0b195-126">Type of managed service identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.CognitiveServices.Models.IdentityType]
Parameter Sets: (All)
Aliases:
Accepted values: None, SystemAssigned, UserAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b195-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0b195-127">-KeyName</span></span>
<span data-ttu-id="0b195-128">Keyvault-keyvault-keyName für Cognitive Services-Konto Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="0b195-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="0b195-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="0b195-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="0b195-130">Gibt an, ob die Schlüsselquelle für die kognitive Dienstkonto Verschlüsselung auf Microsoft. keyvault festgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b195-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="0b195-131">Wenn Sie keyName, keyversion und KeyVaultUri angeben, wird die Schlüsselquelle für das kognitive Dienstkonto auch auf Microsoft festgelegt. keyvault-Wetter dieser Parameter ist festgelegt oder nicht.</span><span class="sxs-lookup"><span data-stu-id="0b195-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="0b195-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="0b195-132">-KeyVaultUri</span></span>
<span data-ttu-id="0b195-133">Kognitive Dienstkonto Verschlüsselung keyvault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="0b195-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="0b195-134">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="0b195-134">-KeyVersion</span></span>
<span data-ttu-id="0b195-135">Keyvault-keyvault-Schlüssel Version für kognitive Dienstkonten Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="0b195-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="0b195-136">-Name</span><span class="sxs-lookup"><span data-stu-id="0b195-136">-Name</span></span>
<span data-ttu-id="0b195-137">Gibt den Namen des zu ändernden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="0b195-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="0b195-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b195-138">-NetworkRuleSet</span></span>
<span data-ttu-id="0b195-139">NetworkRuleSet wird verwendet, um eine Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke zu definieren sowie Werte für Netzwerkeigenschaften festzulegen, beispielsweise zum Behandeln von Anforderungen, die keiner der definierten Regeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0b195-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="0b195-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0b195-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="0b195-141">Der Netzwerkzugriffstyp für das Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="0b195-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="0b195-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b195-142">-ResourceGroupName</span></span>
<span data-ttu-id="0b195-143">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0b195-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="0b195-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0b195-144">-SkuName</span></span>
<span data-ttu-id="0b195-145">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="0b195-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="0b195-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0b195-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b195-147">F0 (﻿Kostenlose Ebene)</span><span class="sxs-lookup"><span data-stu-id="0b195-147">F0 (free tier)</span></span>
- <span data-ttu-id="0b195-148">S0</span><span class="sxs-lookup"><span data-stu-id="0b195-148">S0</span></span>
- <span data-ttu-id="0b195-149">S1</span><span class="sxs-lookup"><span data-stu-id="0b195-149">S1</span></span>
- <span data-ttu-id="0b195-150">S2</span><span class="sxs-lookup"><span data-stu-id="0b195-150">S2</span></span>
- <span data-ttu-id="0b195-151">S3</span><span class="sxs-lookup"><span data-stu-id="0b195-151">S3</span></span>
- <span data-ttu-id="0b195-152">S4</span><span class="sxs-lookup"><span data-stu-id="0b195-152">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b195-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0b195-153">-StorageAccountId</span></span>
<span data-ttu-id="0b195-154">Liste der benutzereigenen Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="0b195-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="0b195-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b195-155">-Tag</span></span>
<span data-ttu-id="0b195-156">Gibt ein Tag als Name-Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="0b195-156">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b195-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b195-157">-Confirm</span></span>
<span data-ttu-id="0b195-158">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b195-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b195-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b195-159">-WhatIf</span></span>
<span data-ttu-id="0b195-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b195-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b195-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b195-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b195-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b195-162">CommonParameters</span></span>
<span data-ttu-id="0b195-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b195-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b195-164">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b195-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b195-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b195-165">INPUTS</span></span>

### <span data-ttu-id="0b195-166">System. String</span><span class="sxs-lookup"><span data-stu-id="0b195-166">System.String</span></span>

### <span data-ttu-id="0b195-167">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="0b195-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="0b195-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b195-168">OUTPUTS</span></span>

### <span data-ttu-id="0b195-169">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0b195-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="0b195-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b195-170">NOTES</span></span>

## <span data-ttu-id="0b195-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b195-171">RELATED LINKS</span></span>

[<span data-ttu-id="0b195-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0b195-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="0b195-173">Neu – AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0b195-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="0b195-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0b195-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
