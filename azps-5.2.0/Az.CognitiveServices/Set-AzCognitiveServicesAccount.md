---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 5cfbfa0452fba4d01d2af5aa8e6acc3a141a4426
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358320"
---
# <span data-ttu-id="9f057-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9f057-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="9f057-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f057-102">SYNOPSIS</span></span>
<span data-ttu-id="9f057-103">Ändert ein Konto.</span><span class="sxs-lookup"><span data-stu-id="9f057-103">Modifies an account.</span></span>

## <span data-ttu-id="9f057-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f057-104">SYNTAX</span></span>

### <span data-ttu-id="9f057-105">CognitiveServicesEncryption (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f057-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f057-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="9f057-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f057-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f057-107">DESCRIPTION</span></span>
<span data-ttu-id="9f057-108">Das **Cmdlet Set-AzCognitiveServicesAccount** ändert die SKU oder Tags des angegebenen Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="9f057-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="9f057-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f057-109">EXAMPLES</span></span>

### <span data-ttu-id="9f057-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9f057-110">Example 1</span></span>
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

## <span data-ttu-id="9f057-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f057-111">PARAMETERS</span></span>

### <span data-ttu-id="9f057-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="9f057-112">-ApiProperty</span></span>
<span data-ttu-id="9f057-113">Die ApiProperties des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="9f057-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="9f057-114">Erforderlich für bestimmte Kontotypen.</span><span class="sxs-lookup"><span data-stu-id="9f057-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="9f057-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9f057-115">-AssignIdentity</span></span>
<span data-ttu-id="9f057-116">Generieren und weisen Sie eine neue Cognitive Services-Kontoidentität für dieses Speicherkonto zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault zu.</span><span class="sxs-lookup"><span data-stu-id="9f057-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="9f057-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="9f057-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="9f057-118">Legen Sie KeySource für die Cognitive Services-Kontoverschlüsselung auf Microsoft.CognitiveServices fest oder nicht.</span><span class="sxs-lookup"><span data-stu-id="9f057-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="9f057-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="9f057-119">-CustomSubdomainName</span></span>
<span data-ttu-id="9f057-120">Cognitive Services Account Subdomain Name.</span><span class="sxs-lookup"><span data-stu-id="9f057-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="9f057-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f057-121">-DefaultProfile</span></span>
<span data-ttu-id="9f057-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9f057-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f057-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9f057-123">-Force</span></span>
<span data-ttu-id="9f057-124">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="9f057-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f057-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9f057-125">-IdentityType</span></span>
<span data-ttu-id="9f057-126">Typ der verwalteten Dienstidentität.</span><span class="sxs-lookup"><span data-stu-id="9f057-126">Type of managed service identity.</span></span>

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

### <span data-ttu-id="9f057-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9f057-127">-KeyName</span></span>
<span data-ttu-id="9f057-128">Cognitive Services Account encryption keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="9f057-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="9f057-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="9f057-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="9f057-130">Legen Sie die Schlüsselquelle für die Verschlüsselung des Cognitive Services-Kontos auf Microsoft.KeyVault fest oder nicht.</span><span class="sxs-lookup"><span data-stu-id="9f057-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="9f057-131">Wenn Sie KeyName, KeyVersion und KeyVaultUri angeben, wird KeySource für die Cognitive Services-Kontoverschlüsselung auch auf "Microsoft.KeyVault" festgelegt, wenn dieser Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9f057-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="9f057-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="9f057-132">-KeyVaultUri</span></span>
<span data-ttu-id="9f057-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="9f057-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="9f057-134">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="9f057-134">-KeyVersion</span></span>
<span data-ttu-id="9f057-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="9f057-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="9f057-136">-Name</span><span class="sxs-lookup"><span data-stu-id="9f057-136">-Name</span></span>
<span data-ttu-id="9f057-137">Gibt den Namen des zu ändernden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="9f057-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="9f057-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9f057-138">-NetworkRuleSet</span></span>
<span data-ttu-id="9f057-139">NetworkRuleSet dient zum Definieren einer Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke sowie zum Festlegen von Werten für Netzwerkeigenschaften, z. B. zum Behandeln von Anforderungen, die keinen der definierten Regeln entsprechen</span><span class="sxs-lookup"><span data-stu-id="9f057-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="9f057-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="9f057-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="9f057-141">Der Netzwerkzugriffstyp für Cognitive Services Account.</span><span class="sxs-lookup"><span data-stu-id="9f057-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="9f057-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f057-142">-ResourceGroupName</span></span>
<span data-ttu-id="9f057-143">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9f057-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="9f057-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9f057-144">-SkuName</span></span>
<span data-ttu-id="9f057-145">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="9f057-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="9f057-146">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="9f057-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f057-147">F0 (kostenlose Stufe)</span><span class="sxs-lookup"><span data-stu-id="9f057-147">F0 (free tier)</span></span>
- <span data-ttu-id="9f057-148">S0</span><span class="sxs-lookup"><span data-stu-id="9f057-148">S0</span></span>
- <span data-ttu-id="9f057-149">S1</span><span class="sxs-lookup"><span data-stu-id="9f057-149">S1</span></span>
- <span data-ttu-id="9f057-150">S2</span><span class="sxs-lookup"><span data-stu-id="9f057-150">S2</span></span>
- <span data-ttu-id="9f057-151">S3</span><span class="sxs-lookup"><span data-stu-id="9f057-151">S3</span></span>
- <span data-ttu-id="9f057-152">S4</span><span class="sxs-lookup"><span data-stu-id="9f057-152">S4</span></span>

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

### <span data-ttu-id="9f057-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9f057-153">-StorageAccountId</span></span>
<span data-ttu-id="9f057-154">Liste der benutzerdefinierten Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="9f057-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="9f057-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f057-155">-Tag</span></span>
<span data-ttu-id="9f057-156">Gibt ein Tag als Name/Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="9f057-156">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="9f057-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f057-157">-Confirm</span></span>
<span data-ttu-id="9f057-158">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f057-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f057-159">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9f057-159">-WhatIf</span></span>
<span data-ttu-id="9f057-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f057-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f057-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f057-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f057-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f057-162">CommonParameters</span></span>
<span data-ttu-id="9f057-163">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f057-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f057-164">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f057-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f057-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f057-165">INPUTS</span></span>

### <span data-ttu-id="9f057-166">System.String</span><span class="sxs-lookup"><span data-stu-id="9f057-166">System.String</span></span>

### <span data-ttu-id="9f057-167">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="9f057-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="9f057-168">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f057-168">OUTPUTS</span></span>

### <span data-ttu-id="9f057-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9f057-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="9f057-170">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9f057-170">NOTES</span></span>

## <span data-ttu-id="9f057-171">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9f057-171">RELATED LINKS</span></span>

[<span data-ttu-id="9f057-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9f057-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="9f057-173">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9f057-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="9f057-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9f057-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
