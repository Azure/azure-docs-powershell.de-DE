---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2c995157b56bafb56df7b385c250b6f7c4fdd4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938979"
---
# <span data-ttu-id="f4934-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f4934-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="f4934-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4934-102">SYNOPSIS</span></span>
<span data-ttu-id="f4934-103">Ändert ein Konto.</span><span class="sxs-lookup"><span data-stu-id="f4934-103">Modifies an account.</span></span>

## <span data-ttu-id="f4934-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4934-104">SYNTAX</span></span>

### <span data-ttu-id="f4934-105">CognitiveServicesEncryption (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4934-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4934-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="f4934-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4934-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4934-107">DESCRIPTION</span></span>
<span data-ttu-id="f4934-108">Das **Cmdlet Set-AzCognitiveServicesAccount** ändert die SKU oder Tags des angegebenen Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="f4934-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="f4934-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4934-109">EXAMPLES</span></span>

### <span data-ttu-id="f4934-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4934-110">Example 1</span></span>
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

## <span data-ttu-id="f4934-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f4934-111">PARAMETERS</span></span>

### <span data-ttu-id="f4934-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="f4934-112">-ApiProperty</span></span>
<span data-ttu-id="f4934-113">Das ApiProperties of Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="f4934-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="f4934-114">Erforderlich für bestimmte Kontotypen.</span><span class="sxs-lookup"><span data-stu-id="f4934-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="f4934-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f4934-115">-AssignIdentity</span></span>
<span data-ttu-id="f4934-116">Generieren und zuweisen Sie eine neue Cognitive Services-Kontoidentität für dieses Speicherkonto für die Verwendung mit wichtigen Verwaltungsdiensten wie Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="f4934-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="f4934-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="f4934-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="f4934-118">Gibt an, ob Cognitive Services Account Encryption KeySource auf Microsoft.CognitiveServices festgelegt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="f4934-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="f4934-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="f4934-119">-CustomSubdomainName</span></span>
<span data-ttu-id="f4934-120">Cognitive Services Account Subdomain Name.</span><span class="sxs-lookup"><span data-stu-id="f4934-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="f4934-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4934-121">-DefaultProfile</span></span>
<span data-ttu-id="f4934-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f4934-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4934-123">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="f4934-123">-Force</span></span>
<span data-ttu-id="f4934-124">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="f4934-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4934-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f4934-125">-IdentityType</span></span>
<span data-ttu-id="f4934-126">Typ der verwalteten Dienstidentität.</span><span class="sxs-lookup"><span data-stu-id="f4934-126">Type of managed service identity.</span></span>

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

### <span data-ttu-id="f4934-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="f4934-127">-KeyName</span></span>
<span data-ttu-id="f4934-128">Cognitive Services Account encryption keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="f4934-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="f4934-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="f4934-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="f4934-130">Gibt an, ob Der Schlüssel für die Verschlüsselung des Cognitive Services-KontosSource auf Microsoft.KeyVault festgelegt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="f4934-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="f4934-131">Wenn Sie KeyName, KeyVersion und KeyVaultUri angeben, wird die KeySource für die Verschlüsselung des Cognitive Services-Kontos auch auf Microsoft.KeyVault festgelegt, wenn dieser Parameter festgelegt ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="f4934-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="f4934-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="f4934-132">-KeyVaultUri</span></span>
<span data-ttu-id="f4934-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="f4934-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="f4934-134">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="f4934-134">-KeyVersion</span></span>
<span data-ttu-id="f4934-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="f4934-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="f4934-136">-Name</span><span class="sxs-lookup"><span data-stu-id="f4934-136">-Name</span></span>
<span data-ttu-id="f4934-137">Gibt den Namen des zu ändernden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f4934-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="f4934-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4934-138">-NetworkRuleSet</span></span>
<span data-ttu-id="f4934-139">NetworkRuleSet wird zum Definieren einer Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke sowie zum Festlegen von Werten für Netzwerkeigenschaften verwendet, z. B. zum Behandeln von Anforderungen, die nicht mit einer der definierten Regeln übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="f4934-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="f4934-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="f4934-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="f4934-141">Der Netzwerkzugriffstyp für Cognitive Services Account.</span><span class="sxs-lookup"><span data-stu-id="f4934-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="f4934-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4934-142">-ResourceGroupName</span></span>
<span data-ttu-id="f4934-143">Gibt den Namen der Ressourcengruppe an, der das Konto zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f4934-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="f4934-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f4934-144">-SkuName</span></span>
<span data-ttu-id="f4934-145">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="f4934-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="f4934-146">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="f4934-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f4934-147">F0 (kostenloser Tarif)</span><span class="sxs-lookup"><span data-stu-id="f4934-147">F0 (free tier)</span></span>
- <span data-ttu-id="f4934-148">S0</span><span class="sxs-lookup"><span data-stu-id="f4934-148">S0</span></span>
- <span data-ttu-id="f4934-149">S1</span><span class="sxs-lookup"><span data-stu-id="f4934-149">S1</span></span>
- <span data-ttu-id="f4934-150">S2</span><span class="sxs-lookup"><span data-stu-id="f4934-150">S2</span></span>
- <span data-ttu-id="f4934-151">S3</span><span class="sxs-lookup"><span data-stu-id="f4934-151">S3</span></span>
- <span data-ttu-id="f4934-152">S4</span><span class="sxs-lookup"><span data-stu-id="f4934-152">S4</span></span>

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

### <span data-ttu-id="f4934-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f4934-153">-StorageAccountId</span></span>
<span data-ttu-id="f4934-154">Liste der benutzerkonteneigenen Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="f4934-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="f4934-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4934-155">-Tag</span></span>
<span data-ttu-id="f4934-156">Gibt ein Tag als Name/Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="f4934-156">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="f4934-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4934-157">-Confirm</span></span>
<span data-ttu-id="f4934-158">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4934-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4934-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4934-159">-WhatIf</span></span>
<span data-ttu-id="f4934-160">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4934-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4934-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4934-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4934-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4934-162">CommonParameters</span></span>
<span data-ttu-id="f4934-163">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4934-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4934-164">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4934-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4934-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4934-165">INPUTS</span></span>

### <span data-ttu-id="f4934-166">System.String</span><span class="sxs-lookup"><span data-stu-id="f4934-166">System.String</span></span>

### <span data-ttu-id="f4934-167">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="f4934-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="f4934-168">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4934-168">OUTPUTS</span></span>

### <span data-ttu-id="f4934-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f4934-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="f4934-170">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f4934-170">NOTES</span></span>

## <span data-ttu-id="f4934-171">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f4934-171">RELATED LINKS</span></span>

[<span data-ttu-id="f4934-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f4934-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="f4934-173">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f4934-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="f4934-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f4934-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
