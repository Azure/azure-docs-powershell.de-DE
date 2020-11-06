---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: ca175d0873b74d8b13d1755f3d0986580c5853ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498938"
---
# <span data-ttu-id="c368d-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c368d-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="c368d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c368d-102">SYNOPSIS</span></span>
<span data-ttu-id="c368d-103">Entfernt alle Berechtigungen für einen Benutzer oder eine Anwendung aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="c368d-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c368d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c368d-104">SYNTAX</span></span>

### <span data-ttu-id="c368d-105">ByUserPrincipalName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c368d-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c368d-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="c368d-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c368d-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c368d-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c368d-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="c368d-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c368d-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="c368d-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c368d-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="c368d-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c368d-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c368d-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c368d-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c368d-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c368d-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="c368d-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c368d-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="c368d-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c368d-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c368d-115">DESCRIPTION</span></span>
<span data-ttu-id="c368d-116">Das Cmdlet **Remove-AzureRmKeyVaultAccessPolicy** entfernt alle Berechtigungen für einen Benutzer oder eine Anwendung oder für alle Benutzer und Anwendungen aus einem Schlüsselspeicher.</span><span class="sxs-lookup"><span data-stu-id="c368d-116">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="c368d-117">Auch wenn Sie alle Berechtigungen entfernen, kann der Besitzer des Azure-Abonnements, das den schlüsseltresor enthält, dem schlüsseltresor Berechtigungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c368d-117">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="c368d-118">Beachten Sie, dass die Angabe der Ressourcengruppe für dieses Cmdlet optional ist, um eine bessere Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="c368d-118">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="c368d-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c368d-119">EXAMPLES</span></span>

### <span data-ttu-id="c368d-120">Beispiel 1: Entfernen von Berechtigungen für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="c368d-120">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="c368d-121">Mit diesem Befehl werden alle Berechtigungen entfernt, die ein Benutzer PattiFuller@contoso.com im schlüsseltresor mit dem Namen Contoso03Vault hat.</span><span class="sxs-lookup"><span data-stu-id="c368d-121">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="c368d-122">Beispiel 2: Entfernen von Berechtigungen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="c368d-122">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="c368d-123">Mit diesem Befehl werden alle Berechtigungen entfernt, die eine Anwendung im schlüsseltresor mit dem Namen Contoso03Vault hat.</span><span class="sxs-lookup"><span data-stu-id="c368d-123">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="c368d-124">In diesem Beispiel wird die Anwendung mit dem in Azure Active Directory registrierten Dienstprinzipalnamen identifiziert http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="c368d-124">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="c368d-125">Beispiel 3: Entfernen von Berechtigungen für eine Anwendung mithilfe der Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="c368d-125">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="c368d-126">Mit diesem Befehl werden alle Berechtigungen entfernt, die eine Anwendung im schlüsseltresor mit dem Namen Contoso03Vault hat.</span><span class="sxs-lookup"><span data-stu-id="c368d-126">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="c368d-127">In diesem Beispiel wird die Anwendung anhand der Objekt-ID des Dienst Prinzipals identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c368d-127">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="c368d-128">Beispiel 4: Entfernen von Berechtigungen für den Microsoft. Compute-Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="c368d-128">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="c368d-129">Dieser Befehl entfernt die Berechtigung für den Microsoft. Compute-Ressourcenanbieter, um Geheimnisse aus der Contoso03Vault zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c368d-129">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="c368d-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="c368d-130">PARAMETERS</span></span>

### <span data-ttu-id="c368d-131">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c368d-131">-ApplicationId</span></span>
<span data-ttu-id="c368d-132">Gibt die ID der Anwendung an, deren Berechtigungen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c368d-132">Specifies the ID of application whose permissions should be removed</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c368d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c368d-133">-DefaultProfile</span></span>
<span data-ttu-id="c368d-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c368d-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c368d-135">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="c368d-135">-EmailAddress</span></span>
<span data-ttu-id="c368d-136">Gibt die e-Mail-Adresse des Benutzers an, dessen Zugriff Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="c368d-136">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail, InputObjectByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c368d-137">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="c368d-137">-EnabledForDeployment</span></span>
<span data-ttu-id="c368d-138">Wenn angegeben, wird der Abruf von Geheimnissen aus diesem schlüsseltresor vom Microsoft. Compute-Ressourcenanbieter deaktiviert, wenn in der Ressourcenerstellung darauf verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c368d-138">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c368d-139">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="c368d-139">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="c368d-140">Wenn angegeben, wird der Abruf von Geheimnissen aus diesem schlüsseltresor durch Azure Disk Encryption deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c368d-140">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c368d-141">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="c368d-141">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="c368d-142">Wenn angegeben, wird der Abruf von Geheimnissen aus diesem schlüsseltresor durch Azure Resource Manager deaktiviert, wenn in Vorlagen darauf verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c368d-142">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c368d-143">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c368d-143">-InputObject</span></span>
<span data-ttu-id="c368d-144">Vault-Schlüsselobjekt</span><span class="sxs-lookup"><span data-stu-id="c368d-144">Key Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c368d-145">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c368d-145">-ObjectId</span></span>
<span data-ttu-id="c368d-146">Gibt die Objekt-ID des Benutzers oder Dienst Prinzipals in Azure Active Directory an, für den Berechtigungen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c368d-146">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c368d-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c368d-147">-PassThru</span></span>
<span data-ttu-id="c368d-148">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c368d-148">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c368d-149">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c368d-149">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c368d-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c368d-150">-ResourceGroupName</span></span>
<span data-ttu-id="c368d-151">Gibt den Namen der Ressourcengruppe an, die dem schlüsseltresor zugeordnet ist, dessen Zugriffsrichtlinie geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c368d-151">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="c368d-152">Wenn dies nicht angegeben ist, sucht dieses Cmdlet nach dem schlüsseltresor im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c368d-152">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c368d-153">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c368d-153">-ServicePrincipalName</span></span>
<span data-ttu-id="c368d-154">Gibt den Dienstprinzipalnamen der Anwendung an, deren Berechtigungen Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="c368d-154">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="c368d-155">Geben Sie die Anwendungs-ID (auch Client-ID genannt) an, die für die Anwendung in Azure Active Directory registriert ist.</span><span class="sxs-lookup"><span data-stu-id="c368d-155">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c368d-156">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c368d-156">-UserPrincipalName</span></span>
<span data-ttu-id="c368d-157">Gibt den Benutzerprinzipalnamen des Benutzers an, dessen Zugriff Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="c368d-157">Specifies the user principal name of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c368d-158">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="c368d-158">-VaultName</span></span>
<span data-ttu-id="c368d-159">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="c368d-159">Specifies the name of the key vault.</span></span>
<span data-ttu-id="c368d-160">Dieses Cmdlet entfernt Berechtigungen für den schlüsseltresor, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c368d-160">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c368d-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c368d-161">-Confirm</span></span>
<span data-ttu-id="c368d-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c368d-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c368d-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c368d-163">-WhatIf</span></span>
<span data-ttu-id="c368d-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c368d-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c368d-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c368d-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c368d-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c368d-166">CommonParameters</span></span>
<span data-ttu-id="c368d-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c368d-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c368d-168">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c368d-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c368d-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c368d-169">INPUTS</span></span>

### <span data-ttu-id="c368d-170">Keine</span><span class="sxs-lookup"><span data-stu-id="c368d-170">None</span></span>
<span data-ttu-id="c368d-171">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c368d-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c368d-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c368d-172">OUTPUTS</span></span>

### <span data-ttu-id="c368d-173">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="c368d-173">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="c368d-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="c368d-174">NOTES</span></span>

## <span data-ttu-id="c368d-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c368d-175">RELATED LINKS</span></span>

[<span data-ttu-id="c368d-176">Satz-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c368d-176">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

