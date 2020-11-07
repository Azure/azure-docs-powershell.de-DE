---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 421a2becff4c32f4c29990f32cbf1a4c6e9a3e84
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848204"
---
# <span data-ttu-id="ea9db-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ea9db-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="ea9db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea9db-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9db-103">Entfernt alle Berechtigungen für einen Benutzer oder eine Anwendung aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="ea9db-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea9db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea9db-104">SYNTAX</span></span>

### <span data-ttu-id="ea9db-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ea9db-105">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea9db-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ea9db-106">ByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea9db-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="ea9db-107">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea9db-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="ea9db-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea9db-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="ea9db-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea9db-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea9db-110">DESCRIPTION</span></span>
<span data-ttu-id="ea9db-111">Das Cmdlet **Remove-AzureRmKeyVaultAccessPolicy** entfernt alle Berechtigungen für einen Benutzer oder eine Anwendung oder für alle Benutzer und Anwendungen aus einem Schlüsselspeicher.</span><span class="sxs-lookup"><span data-stu-id="ea9db-111">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="ea9db-112">Auch wenn Sie alle Berechtigungen entfernen, kann der Besitzer des Azure-Abonnements, das den schlüsseltresor enthält, dem schlüsseltresor Berechtigungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ea9db-112">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="ea9db-113">Beachten Sie, dass die Angabe der Ressourcengruppe für dieses Cmdlet optional ist, um eine bessere Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="ea9db-113">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="ea9db-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea9db-114">EXAMPLES</span></span>

### <span data-ttu-id="ea9db-115">Beispiel 1: Entfernen von Berechtigungen für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="ea9db-115">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="ea9db-116">Mit diesem Befehl werden alle Berechtigungen entfernt, die ein Benutzer PattiFuller@contoso.com im schlüsseltresor mit dem Namen Contoso03Vault hat.</span><span class="sxs-lookup"><span data-stu-id="ea9db-116">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="ea9db-117">Beispiel 2: Entfernen von Berechtigungen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="ea9db-117">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="ea9db-118">Mit diesem Befehl werden alle Berechtigungen entfernt, die eine Anwendung im schlüsseltresor mit dem Namen Contoso03Vault hat.</span><span class="sxs-lookup"><span data-stu-id="ea9db-118">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="ea9db-119">In diesem Beispiel wird die Anwendung mit dem in Azure Active Directory registrierten Dienstprinzipalnamen identifiziert http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="ea9db-119">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="ea9db-120">Beispiel 3: Entfernen von Berechtigungen für eine Anwendung mithilfe der Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="ea9db-120">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="ea9db-121">Mit diesem Befehl werden alle Berechtigungen entfernt, die eine Anwendung im schlüsseltresor mit dem Namen Contoso03Vault hat.</span><span class="sxs-lookup"><span data-stu-id="ea9db-121">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="ea9db-122">In diesem Beispiel wird die Anwendung anhand der Objekt-ID des Dienst Prinzipals identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ea9db-122">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="ea9db-123">Beispiel 4: Entfernen von Berechtigungen für den Microsoft. Compute-Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="ea9db-123">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="ea9db-124">Dieser Befehl entfernt die Berechtigung für den Microsoft. Compute-Ressourcenanbieter, um Geheimnisse aus der Contoso03Vault zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ea9db-124">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="ea9db-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea9db-125">PARAMETERS</span></span>

### <span data-ttu-id="ea9db-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ea9db-126">-ApplicationId</span></span>
<span data-ttu-id="ea9db-127">Für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="ea9db-127">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9db-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea9db-128">-DefaultProfile</span></span>
<span data-ttu-id="ea9db-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ea9db-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea9db-130">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="ea9db-130">-EmailAddress</span></span>
<span data-ttu-id="ea9db-131">Gibt die e-Mail-Adresse des Benutzers an, dessen Zugriff Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="ea9db-131">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9db-132">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="ea9db-132">-EnabledForDeployment</span></span>
<span data-ttu-id="ea9db-133">Ermöglicht es dem Microsoft. Compute-Ressourcenanbieter, Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn bei der Ressourcenerstellung auf diesen schlüsseltresor verwiesen wird, beispielsweise beim Erstellen einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="ea9db-133">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9db-134">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ea9db-134">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="ea9db-135">Aktiviert den Azure Disk Encryption-Dienst, um Geheimnisse zu erhalten und die Schlüssel aus diesem schlüsseltresor zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="ea9db-135">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9db-136">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="ea9db-136">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="ea9db-137">Aktiviert den Azure Resource Manager, um Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn in einer Vorlagenbereitstellung auf diesen schlüsseltresor verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ea9db-137">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9db-138">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="ea9db-138">-ObjectId</span></span>
<span data-ttu-id="ea9db-139">Gibt die Objekt-ID des Benutzers oder Dienst Prinzipals in Azure Active Directory an, für den Berechtigungen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ea9db-139">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9db-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea9db-140">-PassThru</span></span>
<span data-ttu-id="ea9db-141">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ea9db-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ea9db-142">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ea9db-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea9db-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea9db-143">-ResourceGroupName</span></span>
<span data-ttu-id="ea9db-144">Gibt den Namen der Ressourcengruppe an, die dem schlüsseltresor zugeordnet ist, dessen Zugriffsrichtlinie geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ea9db-144">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="ea9db-145">Wenn dies nicht angegeben ist, sucht dieses Cmdlet nach dem schlüsseltresor im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea9db-145">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9db-146">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ea9db-146">-ServicePrincipalName</span></span>
<span data-ttu-id="ea9db-147">Gibt den Dienstprinzipalnamen der Anwendung an, deren Berechtigungen Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="ea9db-147">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="ea9db-148">Geben Sie die Anwendungs-ID (auch Client-ID genannt) an, die für die Anwendung in Azure Active Directory registriert ist.</span><span class="sxs-lookup"><span data-stu-id="ea9db-148">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9db-149">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ea9db-149">-UserPrincipalName</span></span>
<span data-ttu-id="ea9db-150">Gibt den Benutzerprinzipalnamen des Benutzers an, dessen Zugriff Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="ea9db-150">Specifies the user principal name of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9db-151">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="ea9db-151">-VaultName</span></span>
<span data-ttu-id="ea9db-152">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="ea9db-152">Specifies the name of the key vault.</span></span>
<span data-ttu-id="ea9db-153">Dieses Cmdlet entfernt Berechtigungen für den schlüsseltresor, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ea9db-153">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea9db-154">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea9db-154">-Confirm</span></span>
<span data-ttu-id="ea9db-155">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea9db-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea9db-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea9db-156">-WhatIf</span></span>
<span data-ttu-id="ea9db-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea9db-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea9db-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea9db-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea9db-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9db-159">CommonParameters</span></span>
<span data-ttu-id="ea9db-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea9db-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9db-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea9db-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9db-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea9db-162">INPUTS</span></span>

## <span data-ttu-id="ea9db-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea9db-163">OUTPUTS</span></span>

### <span data-ttu-id="ea9db-164">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="ea9db-164">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="ea9db-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea9db-165">NOTES</span></span>

## <span data-ttu-id="ea9db-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea9db-166">RELATED LINKS</span></span>

[<span data-ttu-id="ea9db-167">Satz-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ea9db-167">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

