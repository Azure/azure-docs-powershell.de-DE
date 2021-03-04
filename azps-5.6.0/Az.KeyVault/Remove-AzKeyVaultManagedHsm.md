---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: ac778148f90d90caf52fdb3c029376daf4470069
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938656"
---
# <span data-ttu-id="c8935-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="c8935-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="c8935-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8935-102">SYNOPSIS</span></span>
<span data-ttu-id="c8935-103">Löscht ein verwaltetes HSM.</span><span class="sxs-lookup"><span data-stu-id="c8935-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="c8935-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8935-104">SYNTAX</span></span>

### <span data-ttu-id="c8935-105">RemoveManagedHsmByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8935-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8935-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="c8935-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8935-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="c8935-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8935-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8935-108">DESCRIPTION</span></span>
<span data-ttu-id="c8935-109">Das **Cmdlet Remove-AzKeyVaultManagedHsm** löscht das angegebene verwaltete HSM.</span><span class="sxs-lookup"><span data-stu-id="c8935-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="c8935-110">Außerdem werden alle schlüssel gelöscht, die in dieser Instanz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c8935-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="c8935-111">Beachten Sie, dass die Angabe der Ressourcengruppe für dieses Cmdlet zwar optional ist, Sie dies aber für eine bessere Leistung tun sollten.</span><span class="sxs-lookup"><span data-stu-id="c8935-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="c8935-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c8935-112">EXAMPLES</span></span>

### <span data-ttu-id="c8935-113">Beispiel 1: Entfernen eines verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="c8935-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="c8935-114">Mit diesem Befehl wird der verwaltete Hsm mit dem Namen myhsm aus Ihrem aktuellen Abonnement entfernt.</span><span class="sxs-lookup"><span data-stu-id="c8935-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="c8935-115">Beispiel 2: Entfernen eines verwalteten Hsms aus einer angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c8935-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="c8935-116">Mit diesem Befehl wird der verwaltete Hsm mit dem Namen myhsm aus der Ressourcengruppe mit dem Namen myrg1 entfernt.</span><span class="sxs-lookup"><span data-stu-id="c8935-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="c8935-117">Wenn Sie den Namen der Ressourcengruppe nicht angeben, sucht das Cmdlet nach dem benannten verwalteten HSM, das in Ihrem aktuellen Abonnement gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8935-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="c8935-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c8935-118">PARAMETERS</span></span>

### <span data-ttu-id="c8935-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8935-119">-AsJob</span></span>
<span data-ttu-id="c8935-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c8935-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8935-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8935-121">-DefaultProfile</span></span>
<span data-ttu-id="c8935-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8935-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8935-123">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="c8935-123">-Force</span></span>
<span data-ttu-id="c8935-124">Gibt an, dass sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="c8935-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="c8935-125">Standardmäßig werden Sie in diesem Cmdlet aufgefordert, zu bestätigen, dass Sie das verwaltete HSM löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="c8935-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="c8935-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8935-126">-InputObject</span></span>
<span data-ttu-id="c8935-127">Verwaltetes HSM-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8935-127">Managed HSM object to be deleted.</span></span>

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

### <span data-ttu-id="c8935-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c8935-128">-Name</span></span>
<span data-ttu-id="c8935-129">Gibt den Namen des verwalteten HSM an, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8935-129">Specifies the name of the managed HSM to remove.</span></span>

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

### <span data-ttu-id="c8935-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8935-130">-PassThru</span></span>
<span data-ttu-id="c8935-131">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c8935-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c8935-132">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c8935-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c8935-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8935-133">-ResourceGroupName</span></span>
<span data-ttu-id="c8935-134">Gibt den Namen der Ressourcengruppe für azure verwaltetes HSM an, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8935-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

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

### <span data-ttu-id="c8935-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8935-135">-ResourceId</span></span>
<span data-ttu-id="c8935-136">ManagedHsm Resource Id.</span><span class="sxs-lookup"><span data-stu-id="c8935-136">ManagedHsm Resource Id.</span></span>

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

### <span data-ttu-id="c8935-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8935-137">-Confirm</span></span>
<span data-ttu-id="c8935-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8935-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8935-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8935-139">-WhatIf</span></span>
<span data-ttu-id="c8935-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8935-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8935-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8935-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8935-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8935-142">CommonParameters</span></span>
<span data-ttu-id="c8935-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8935-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8935-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8935-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8935-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c8935-145">INPUTS</span></span>

### <span data-ttu-id="c8935-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="c8935-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="c8935-147">System.String</span><span class="sxs-lookup"><span data-stu-id="c8935-147">System.String</span></span>

## <span data-ttu-id="c8935-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c8935-148">OUTPUTS</span></span>

### <span data-ttu-id="c8935-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8935-149">System.Boolean</span></span>

## <span data-ttu-id="c8935-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c8935-150">NOTES</span></span>

## <span data-ttu-id="c8935-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c8935-151">RELATED LINKS</span></span>

[<span data-ttu-id="c8935-152">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="c8935-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="c8935-153">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="c8935-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="c8935-154">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="c8935-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)