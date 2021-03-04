---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 6f4ddcb358c2ebc0789bb96508feacb69449d17d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931091"
---
# <span data-ttu-id="d1770-101">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d1770-101">Update-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="d1770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1770-102">SYNOPSIS</span></span>
<span data-ttu-id="d1770-103">Aktualisieren Sie den Zustand eines von Azure verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="d1770-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="d1770-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1770-104">SYNTAX</span></span>

### <span data-ttu-id="d1770-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1770-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVaultManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1770-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1770-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1770-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1770-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1770-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1770-108">DESCRIPTION</span></span>
<span data-ttu-id="d1770-109">Dieses Cmdlet aktualisiert den Zustand eines von Azure verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="d1770-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="d1770-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d1770-110">EXAMPLES</span></span>

### <span data-ttu-id="d1770-111">Beispiel 1: Direktes Aktualisieren eines verwalteten Hsms</span><span class="sxs-lookup"><span data-stu-id="d1770-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

Managed HSM Name                    : testmhsm
Resource Group Name                 : testmhsm
Location                            : eastus2euap
Resource ID                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testmhsm/provid
                                      ers/Microsoft.KeyVault/managedHSMs/testmhsm
HSM Pool URI                        :
Tenant ID                           : xxxxxx-xxxx-xxxx-xxxxxxxxxxxx
Initial Admin Object Ids            : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SKU                                 : StandardB1
Soft Delete Enabled?                : True
Enabled Purge Protection?           : False
Soft Delete Retention Period (days) : 90
Provisioning State                  : Provisioning
Status Message                      : Resource creation in progress. Starting service...
Tags                                :
                                      Name        Value
                                      ====        =====
                                      testKey     testValued
```

<span data-ttu-id="d1770-112">Aktualisiert Tags für den verwalteten Hsm, der `$hsmName` in der Ressourcengruppe benannt `$resourceGroupName` ist.</span><span class="sxs-lookup"><span data-stu-id="d1770-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="d1770-113">Beispiel 2: Aktualisieren eines verwalteten Hsms mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="d1770-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzKeyVaultManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="d1770-114">Aktualisiert Tags für das verwaltete Hsm mithilfe der Pipingsyntax.</span><span class="sxs-lookup"><span data-stu-id="d1770-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="d1770-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d1770-115">PARAMETERS</span></span>

### <span data-ttu-id="d1770-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1770-116">-DefaultProfile</span></span>
<span data-ttu-id="d1770-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1770-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1770-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1770-118">-InputObject</span></span>
<span data-ttu-id="d1770-119">Verwaltetes HSM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d1770-119">Managed HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1770-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d1770-120">-Name</span></span>
<span data-ttu-id="d1770-121">Name des verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="d1770-121">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1770-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1770-122">-ResourceGroupName</span></span>
<span data-ttu-id="d1770-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d1770-123">Name of the resource group.</span></span>

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

### <span data-ttu-id="d1770-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1770-124">-ResourceId</span></span>
<span data-ttu-id="d1770-125">Ressourcen-ID des verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="d1770-125">Resource ID of the managed HSM.</span></span>

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

### <span data-ttu-id="d1770-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1770-126">-Tag</span></span>
<span data-ttu-id="d1770-127">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="d1770-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="d1770-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1770-128">-Confirm</span></span>
<span data-ttu-id="d1770-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1770-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1770-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1770-130">-WhatIf</span></span>
<span data-ttu-id="d1770-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1770-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1770-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1770-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1770-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1770-133">CommonParameters</span></span>
<span data-ttu-id="d1770-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1770-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1770-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1770-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1770-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d1770-136">INPUTS</span></span>

### <span data-ttu-id="d1770-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d1770-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="d1770-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d1770-138">System.String</span></span>

### <span data-ttu-id="d1770-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d1770-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d1770-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d1770-140">OUTPUTS</span></span>

### <span data-ttu-id="d1770-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d1770-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="d1770-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d1770-142">NOTES</span></span>

## <span data-ttu-id="d1770-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d1770-143">RELATED LINKS</span></span>

[<span data-ttu-id="d1770-144">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d1770-144">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="d1770-145">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d1770-145">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="d1770-146">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d1770-146">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)