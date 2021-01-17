---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 0c7e22174b0306a3b9b5a37bd99edeb06f124334
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473171"
---
# <span data-ttu-id="501a8-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="501a8-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="501a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="501a8-102">SYNOPSIS</span></span>
<span data-ttu-id="501a8-103">Erstellt ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="501a8-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="501a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="501a8-104">SYNTAX</span></span>

### <span data-ttu-id="501a8-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="501a8-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="501a8-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="501a8-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="501a8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="501a8-107">DESCRIPTION</span></span>
<span data-ttu-id="501a8-108">Das **Cmdlet "New-AzCognitiveServicesAccount"** erstellt ein Cognitive Services-Konto mit dem angegebenen Typ und der angegebenen SKU.</span><span class="sxs-lookup"><span data-stu-id="501a8-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="501a8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="501a8-109">EXAMPLES</span></span>

### <span data-ttu-id="501a8-110">1:</span><span class="sxs-lookup"><span data-stu-id="501a8-110">1:</span></span>
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

## <span data-ttu-id="501a8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="501a8-111">PARAMETERS</span></span>

### <span data-ttu-id="501a8-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="501a8-112">-ApiProperty</span></span>
<span data-ttu-id="501a8-113">Die ApiProperties des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="501a8-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="501a8-114">Erforderlich für bestimmte Kontotypen.</span><span class="sxs-lookup"><span data-stu-id="501a8-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="501a8-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="501a8-115">-AssignIdentity</span></span>
<span data-ttu-id="501a8-116">Generieren und weisen Sie eine neue Cognitive Services-Kontoidentität für dieses Speicherkonto zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault zu.</span><span class="sxs-lookup"><span data-stu-id="501a8-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="501a8-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="501a8-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="501a8-118">Legen Sie die KeySource für die Verschlüsselung des Cognitive Services-Kontos auf Microsoft.CognitiveServices fest oder nicht.</span><span class="sxs-lookup"><span data-stu-id="501a8-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="501a8-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="501a8-119">-CustomSubdomainName</span></span>
<span data-ttu-id="501a8-120">Cognitive Services Account Subdomain Name.</span><span class="sxs-lookup"><span data-stu-id="501a8-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="501a8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="501a8-121">-DefaultProfile</span></span>
<span data-ttu-id="501a8-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="501a8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="501a8-123">-Force</span><span class="sxs-lookup"><span data-stu-id="501a8-123">-Force</span></span>
<span data-ttu-id="501a8-124">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="501a8-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="501a8-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="501a8-125">-KeyName</span></span>
<span data-ttu-id="501a8-126">Cognitive Services Account encryption keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="501a8-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="501a8-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="501a8-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="501a8-128">Legen Sie die Schlüsselquelle für die Verschlüsselung des Cognitive Services-Kontos auf Microsoft.KeyVault fest oder nicht.</span><span class="sxs-lookup"><span data-stu-id="501a8-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="501a8-129">Wenn Sie KeyName, KeyVersion und KeyVaultUri angeben, wird KeySource für die Cognitive Services-Kontoverschlüsselung auch auf "Microsoft.KeyVault" festgelegt, wenn dieser Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="501a8-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="501a8-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="501a8-130">-KeyVaultUri</span></span>
<span data-ttu-id="501a8-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="501a8-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="501a8-132">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="501a8-132">-KeyVersion</span></span>
<span data-ttu-id="501a8-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="501a8-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="501a8-134">-Location</span><span class="sxs-lookup"><span data-stu-id="501a8-134">-Location</span></span>
<span data-ttu-id="501a8-135">Gibt den Speicherort an, an dem das Konto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="501a8-135">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="501a8-136">-Name</span><span class="sxs-lookup"><span data-stu-id="501a8-136">-Name</span></span>
<span data-ttu-id="501a8-137">Gibt den Namen für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="501a8-137">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="501a8-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="501a8-138">-NetworkRuleSet</span></span>
<span data-ttu-id="501a8-139">NetworkRuleSet dient zum Definieren einer Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke sowie zum Festlegen von Werten für Netzwerkeigenschaften, z. B. zum Behandeln von Anforderungen, die keinen der definierten Regeln entsprechen</span><span class="sxs-lookup"><span data-stu-id="501a8-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="501a8-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="501a8-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="501a8-141">Der Netzwerkzugriffstyp für Cognitive Services Account.</span><span class="sxs-lookup"><span data-stu-id="501a8-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="501a8-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="501a8-142">-ResourceGroupName</span></span>
<span data-ttu-id="501a8-143">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="501a8-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="501a8-144">Die Ressourcengruppe muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="501a8-144">The resource group must already exist.</span></span>

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

### <span data-ttu-id="501a8-145">-SkuName</span><span class="sxs-lookup"><span data-stu-id="501a8-145">-SkuName</span></span>
<span data-ttu-id="501a8-146">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="501a8-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="501a8-147">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="501a8-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="501a8-148">F0 (kostenlose Stufe)</span><span class="sxs-lookup"><span data-stu-id="501a8-148">F0 (free tier)</span></span>
- <span data-ttu-id="501a8-149">S0</span><span class="sxs-lookup"><span data-stu-id="501a8-149">S0</span></span>
- <span data-ttu-id="501a8-150">S1</span><span class="sxs-lookup"><span data-stu-id="501a8-150">S1</span></span>
- <span data-ttu-id="501a8-151">S2</span><span class="sxs-lookup"><span data-stu-id="501a8-151">S2</span></span>
- <span data-ttu-id="501a8-152">S3</span><span class="sxs-lookup"><span data-stu-id="501a8-152">S3</span></span>
- <span data-ttu-id="501a8-153">S4 Weitere Informationen finden Sie unter [Cognitive Service-APIs.](https://www.microsoft.com/cognitive-services/en-us/apis)</span><span class="sxs-lookup"><span data-stu-id="501a8-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="501a8-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="501a8-154">-StorageAccountId</span></span>
<span data-ttu-id="501a8-155">Liste der benutzerdefinierten Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="501a8-155">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="501a8-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="501a8-156">-Tag</span></span>
<span data-ttu-id="501a8-157">Gibt ein Tag als Name/Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="501a8-157">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="501a8-158">-Type</span><span class="sxs-lookup"><span data-stu-id="501a8-158">-Type</span></span>
<span data-ttu-id="501a8-159">Gibt den Typ des zu erstellenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="501a8-159">Specifies the type of account to create.</span></span> <span data-ttu-id="501a8-160">Verwenden `Get-AzCognitiveServicesAccountType` Sie das Cmdlet, um die aktuellen zulässigen Werte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="501a8-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="501a8-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="501a8-161">-Confirm</span></span>
<span data-ttu-id="501a8-162">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="501a8-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="501a8-163">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="501a8-163">-WhatIf</span></span>
<span data-ttu-id="501a8-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="501a8-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="501a8-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="501a8-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="501a8-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="501a8-166">CommonParameters</span></span>
<span data-ttu-id="501a8-167">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="501a8-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="501a8-168">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="501a8-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="501a8-169">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="501a8-169">INPUTS</span></span>

### <span data-ttu-id="501a8-170">System.String</span><span class="sxs-lookup"><span data-stu-id="501a8-170">System.String</span></span>

## <span data-ttu-id="501a8-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="501a8-171">OUTPUTS</span></span>

### <span data-ttu-id="501a8-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="501a8-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="501a8-173">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="501a8-173">NOTES</span></span>

## <span data-ttu-id="501a8-174">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="501a8-174">RELATED LINKS</span></span>

[<span data-ttu-id="501a8-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="501a8-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="501a8-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="501a8-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="501a8-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="501a8-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
