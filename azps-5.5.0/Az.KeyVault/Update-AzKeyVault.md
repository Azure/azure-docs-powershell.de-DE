---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 2a9c2870e0ce33b93d3013e84e7de3642b42708c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152652"
---
# <span data-ttu-id="a644b-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a644b-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="a644b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a644b-102">SYNOPSIS</span></span>
<span data-ttu-id="a644b-103">Aktualisieren Sie den Zustand eines Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a644b-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="a644b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a644b-104">SYNTAX</span></span>

### <span data-ttu-id="a644b-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a644b-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a644b-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a644b-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a644b-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a644b-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a644b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a644b-108">DESCRIPTION</span></span>
<span data-ttu-id="a644b-109">Dieses Cmdlet aktualisiert den Zustand eines Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a644b-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="a644b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a644b-110">EXAMPLES</span></span>

### <span data-ttu-id="a644b-111">Beispiel 1: Aktivieren des Reinigungsschutzes</span><span class="sxs-lookup"><span data-stu-id="a644b-111">Example 1： Enable purge protection</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="a644b-112">Aktiviert den Reinigungsschutz mithilfe der Pipingsyntax.</span><span class="sxs-lookup"><span data-stu-id="a644b-112">Enables purge protection using piping syntax.</span></span>

### <span data-ttu-id="a644b-113">Beispiel 2: Aktivieren der RBAC-Autorisierung</span><span class="sxs-lookup"><span data-stu-id="a644b-113">Example 2： Enable RBAC Authorization</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnableRbacAuthorization $true
```

<span data-ttu-id="a644b-114">Aktiviert die #A0 mithilfe der Pipingsyntax.</span><span class="sxs-lookup"><span data-stu-id="a644b-114">Enables RBAC Authorization using piping syntax.</span></span>

### <span data-ttu-id="a644b-115">Beispiel 3: Festlegen von Tags</span><span class="sxs-lookup"><span data-stu-id="a644b-115">Example 3： Set tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{key = "value"}
```

<span data-ttu-id="a644b-116">Legt die Tags eines Schlüsseltresor namens "$keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="a644b-116">Sets the tags of a key vault named $keyVaultName.</span></span>

### <span data-ttu-id="a644b-117">Beispiel 4: Klare Tags</span><span class="sxs-lookup"><span data-stu-id="a644b-117">Example 4： Clean tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{}
```

<span data-ttu-id="a644b-118">Löscht alle Tags eines Schlüsseltresor namens $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="a644b-118">Deletes all tags of a key vault named $keyVaultName.</span></span>

## <span data-ttu-id="a644b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a644b-119">PARAMETERS</span></span>

### <span data-ttu-id="a644b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a644b-120">-DefaultProfile</span></span>
<span data-ttu-id="a644b-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a644b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a644b-122">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="a644b-122">-EnablePurgeProtection</span></span>
<span data-ttu-id="a644b-123">Aktivieren Sie die Reinigungsschutzfunktion für diesen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="a644b-123">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="a644b-124">Nach der Aktivierung kann sie nicht mehr deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a644b-124">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="a644b-125">Dies setzt voraus, dass das weiche Löschen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a644b-125">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="a644b-126">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="a644b-126">-EnableRbacAuthorization</span></span>
<span data-ttu-id="a644b-127">Aktivieren oder deaktivieren Sie diesen Schlüsseltresor, um Datenaktionen nach rollenbasierter Zugriffssteuerung (Role Based Access Control, RBAC) zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="a644b-127">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a644b-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a644b-128">-InputObject</span></span>
<span data-ttu-id="a644b-129">Schlüsseltresorobjekt.</span><span class="sxs-lookup"><span data-stu-id="a644b-129">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a644b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a644b-130">-ResourceGroupName</span></span>
<span data-ttu-id="a644b-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a644b-131">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a644b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a644b-132">-ResourceId</span></span>
<span data-ttu-id="a644b-133">Ressourcen-ID des Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="a644b-133">Resource ID of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a644b-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="a644b-134">-Tag</span></span>
<span data-ttu-id="a644b-135">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="a644b-135">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a644b-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a644b-136">-VaultName</span></span>
<span data-ttu-id="a644b-137">Der Name des Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="a644b-137">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a644b-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a644b-138">-Confirm</span></span>
<span data-ttu-id="a644b-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a644b-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a644b-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a644b-140">-WhatIf</span></span>
<span data-ttu-id="a644b-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a644b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a644b-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a644b-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a644b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a644b-143">CommonParameters</span></span>
<span data-ttu-id="a644b-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a644b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a644b-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a644b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a644b-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a644b-146">INPUTS</span></span>

### <span data-ttu-id="a644b-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a644b-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a644b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a644b-148">System.String</span></span>

## <span data-ttu-id="a644b-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a644b-149">OUTPUTS</span></span>

### <span data-ttu-id="a644b-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a644b-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="a644b-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a644b-151">NOTES</span></span>

## <span data-ttu-id="a644b-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a644b-152">RELATED LINKS</span></span>
