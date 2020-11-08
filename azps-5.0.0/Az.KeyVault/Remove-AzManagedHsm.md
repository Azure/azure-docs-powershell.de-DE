---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
ms.openlocfilehash: 6555299726d8dcf443382f72c2aba6324b6b377d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175500"
---
# <span data-ttu-id="3c8a1-101">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="3c8a1-101">Remove-AzManagedHsm</span></span>

## <span data-ttu-id="3c8a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c8a1-102">SYNOPSIS</span></span>
<span data-ttu-id="3c8a1-103">Löscht ein verwaltetes HSM.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="3c8a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c8a1-104">SYNTAX</span></span>

### <span data-ttu-id="3c8a1-105">RemoveManagedHsmByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3c8a1-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c8a1-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="3c8a1-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c8a1-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c8a1-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c8a1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c8a1-108">DESCRIPTION</span></span>
<span data-ttu-id="3c8a1-109">Das Cmdlet **Remove-AzManagedHsm** löscht das angegebene verwaltete HSM.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-109">The **Remove-AzManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="3c8a1-110">Außerdem werden alle in dieser Instanz enthaltenen Schlüssel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="3c8a1-111">Beachten Sie, dass Sie eine bessere Leistung erzielen sollten, wenn Sie die Ressourcengruppe für dieses Cmdlet optional angeben.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="3c8a1-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c8a1-112">EXAMPLES</span></span>

### <span data-ttu-id="3c8a1-113">Beispiel 1: Entfernen eines verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="3c8a1-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="3c8a1-114">Dieser Befehl entfernt das verwaltete HSM mit dem Namen myhsm aus Ihrem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="3c8a1-115">Beispiel 2: Entfernen eines verwalteten HSM aus einer angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3c8a1-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="3c8a1-116">Dieser Befehl entfernt das verwaltete HSM mit dem Namen myhsm aus der Ressourcengruppe mit dem Namen myrg1.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="3c8a1-117">Wenn Sie den Namen der Ressourcengruppe nicht angeben, sucht das Cmdlet nach dem benannten verwalteten HSM, das Sie in Ihrem aktuellen Abonnement löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="3c8a1-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c8a1-118">PARAMETERS</span></span>

### <span data-ttu-id="3c8a1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c8a1-119">-AsJob</span></span>
<span data-ttu-id="3c8a1-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3c8a1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c8a1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c8a1-121">-DefaultProfile</span></span>
<span data-ttu-id="3c8a1-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c8a1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3c8a1-123">-Force</span></span>
<span data-ttu-id="3c8a1-124">Gibt an, dass das Cmdlet Sie nicht zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="3c8a1-125">Standardmäßig werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, dass Sie das verwaltete HSM löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="3c8a1-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3c8a1-126">-InputObject</span></span>
<span data-ttu-id="3c8a1-127">Verwaltetes HSM-Objekt, das gelöscht werden soll</span><span class="sxs-lookup"><span data-stu-id="3c8a1-127">Managed HSM object to be deleted.</span></span>

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

### <span data-ttu-id="3c8a1-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3c8a1-128">-Name</span></span>
<span data-ttu-id="3c8a1-129">Gibt den Namen des verwalteten HSM an, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-129">Specifies the name of the managed HSM to remove.</span></span>

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

### <span data-ttu-id="3c8a1-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c8a1-130">-PassThru</span></span>
<span data-ttu-id="3c8a1-131">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3c8a1-132">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3c8a1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c8a1-133">-ResourceGroupName</span></span>
<span data-ttu-id="3c8a1-134">Gibt den Namen der Ressourcengruppe an, die von Azure Managed HSM entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

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

### <span data-ttu-id="3c8a1-135">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3c8a1-135">-ResourceId</span></span>
<span data-ttu-id="3c8a1-136">ManagedHsm-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-136">ManagedHsm Resource Id.</span></span>

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

### <span data-ttu-id="3c8a1-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3c8a1-137">-Confirm</span></span>
<span data-ttu-id="3c8a1-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c8a1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c8a1-139">-WhatIf</span></span>
<span data-ttu-id="3c8a1-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c8a1-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c8a1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c8a1-142">CommonParameters</span></span>
<span data-ttu-id="3c8a1-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c8a1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c8a1-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c8a1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c8a1-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c8a1-145">INPUTS</span></span>

### <span data-ttu-id="3c8a1-146">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="3c8a1-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="3c8a1-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3c8a1-147">System.String</span></span>

## <span data-ttu-id="3c8a1-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c8a1-148">OUTPUTS</span></span>

### <span data-ttu-id="3c8a1-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c8a1-149">System.Boolean</span></span>

## <span data-ttu-id="3c8a1-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c8a1-150">NOTES</span></span>

## <span data-ttu-id="3c8a1-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c8a1-151">RELATED LINKS</span></span>

[<span data-ttu-id="3c8a1-152">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="3c8a1-152">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="3c8a1-153">Neu – AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="3c8a1-153">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="3c8a1-154">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="3c8a1-154">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)