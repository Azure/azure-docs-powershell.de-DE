---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 82521bd7d0ff4f34f68029cdb7faacdd198f2b02
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167217"
---
# <span data-ttu-id="7845f-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7845f-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="7845f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7845f-102">SYNOPSIS</span></span>
<span data-ttu-id="7845f-103">Löscht einen verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="7845f-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="7845f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7845f-104">SYNTAX</span></span>

### <span data-ttu-id="7845f-105">RemoveManagedHsmByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7845f-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7845f-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="7845f-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7845f-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="7845f-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7845f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7845f-108">DESCRIPTION</span></span>
<span data-ttu-id="7845f-109">Das **Cmdlet "Remove-AzKeyVaultManagedHsm"** löscht das angegebene verwaltete HSM.</span><span class="sxs-lookup"><span data-stu-id="7845f-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="7845f-110">Außerdem werden alle in dieser Instanz enthaltenen Schlüssel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7845f-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="7845f-111">Beachten Sie: Obwohl die Angabe der Ressourcengruppe für dieses Cmdlet optional ist, sollten Sie dies für eine bessere Leistung tun.</span><span class="sxs-lookup"><span data-stu-id="7845f-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="7845f-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7845f-112">EXAMPLES</span></span>

### <span data-ttu-id="7845f-113">Beispiel 1: Entfernen eines verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="7845f-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="7845f-114">Mit diesem Befehl wird der verwaltete Hsm namens "myhsm" aus Ihrem aktuellen Abonnement entfernt.</span><span class="sxs-lookup"><span data-stu-id="7845f-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="7845f-115">Beispiel 2: Entfernen eines verwalteten HSM aus einer angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7845f-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="7845f-116">Mit diesem Befehl wird der verwaltete HSM mit dem Namen "myhsm" aus der Ressourcengruppe "myrg1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="7845f-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="7845f-117">Wenn Sie den Namen der Ressourcengruppe nicht angeben, sucht das Cmdlet nach dem benannten verwalteten HSM, das in Ihrem aktuellen Abonnement gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7845f-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="7845f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7845f-118">PARAMETERS</span></span>

### <span data-ttu-id="7845f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7845f-119">-AsJob</span></span>
<span data-ttu-id="7845f-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7845f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7845f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7845f-121">-DefaultProfile</span></span>
<span data-ttu-id="7845f-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7845f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7845f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7845f-123">-Force</span></span>
<span data-ttu-id="7845f-124">Zeigt an, dass sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="7845f-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="7845f-125">Standardmäßig werden Sie von diesem Cmdlet aufgefordert zu bestätigen, dass Sie den verwalteten HSM löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="7845f-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="7845f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7845f-126">-InputObject</span></span>
<span data-ttu-id="7845f-127">Verwaltetes HSM-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7845f-127">Managed HSM object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: RemoveManagedHsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7845f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="7845f-128">-Name</span></span>
<span data-ttu-id="7845f-129">Gibt den Namen des verwalteten HSM an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7845f-129">Specifies the name of the managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7845f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7845f-130">-PassThru</span></span>
<span data-ttu-id="7845f-131">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="7845f-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7845f-132">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="7845f-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7845f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7845f-133">-ResourceGroupName</span></span>
<span data-ttu-id="7845f-134">Gibt den Namen der Ressourcengruppe an, die von Azure verwalteten HSM entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7845f-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7845f-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7845f-135">-ResourceId</span></span>
<span data-ttu-id="7845f-136">VerwalteteHsm-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7845f-136">ManagedHsm Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7845f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7845f-137">-Confirm</span></span>
<span data-ttu-id="7845f-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7845f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7845f-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7845f-139">-WhatIf</span></span>
<span data-ttu-id="7845f-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7845f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7845f-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7845f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7845f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7845f-142">CommonParameters</span></span>
<span data-ttu-id="7845f-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7845f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7845f-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7845f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7845f-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7845f-145">INPUTS</span></span>

### <span data-ttu-id="7845f-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7845f-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="7845f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7845f-147">System.String</span></span>

## <span data-ttu-id="7845f-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7845f-148">OUTPUTS</span></span>

### <span data-ttu-id="7845f-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7845f-149">System.Boolean</span></span>

## <span data-ttu-id="7845f-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7845f-150">NOTES</span></span>

## <span data-ttu-id="7845f-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7845f-151">RELATED LINKS</span></span>

[<span data-ttu-id="7845f-152">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7845f-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="7845f-153">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7845f-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="7845f-154">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7845f-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)