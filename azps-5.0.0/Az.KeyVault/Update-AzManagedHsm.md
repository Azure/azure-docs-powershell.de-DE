---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
ms.openlocfilehash: 49e8e5aeddba1b15c97155a200413ea774c8a7a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180393"
---
# <span data-ttu-id="a0ecc-101">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a0ecc-101">Update-AzManagedHsm</span></span>

## <span data-ttu-id="a0ecc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ecc-103">Aktualisieren Sie den Zustand eines Azure Managed HSM.</span><span class="sxs-lookup"><span data-stu-id="a0ecc-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="a0ecc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0ecc-104">SYNTAX</span></span>

### <span data-ttu-id="a0ecc-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ecc-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0ecc-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0ecc-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0ecc-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0ecc-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0ecc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0ecc-108">DESCRIPTION</span></span>
<span data-ttu-id="a0ecc-109">Dieses Cmdlet aktualisiert den Zustand eines Azure Managed HSM.</span><span class="sxs-lookup"><span data-stu-id="a0ecc-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="a0ecc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0ecc-110">EXAMPLES</span></span>

### <span data-ttu-id="a0ecc-111">Beispiel 1: Direktes Aktualisieren eines verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="a0ecc-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

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

<span data-ttu-id="a0ecc-112">Aktualisiert Tags für das verwaltete HSM `$hsmName` , das in der Ressourcengruppe benannt ist `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="a0ecc-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="a0ecc-113">Beispiel 2: Aktualisieren eines verwalteten HSM mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="a0ecc-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="a0ecc-114">Aktualisiert Tags für das verwaltete HSM mithilfe der Piping-Syntax.</span><span class="sxs-lookup"><span data-stu-id="a0ecc-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="a0ecc-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0ecc-115">PARAMETERS</span></span>

### <span data-ttu-id="a0ecc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ecc-116">-DefaultProfile</span></span>
<span data-ttu-id="a0ecc-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0ecc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0ecc-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a0ecc-118">-InputObject</span></span>
<span data-ttu-id="a0ecc-119">Verwaltetes HSM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a0ecc-119">Managed HSM object.</span></span>

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

### <span data-ttu-id="a0ecc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a0ecc-120">-Name</span></span>
<span data-ttu-id="a0ecc-121">Name des verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="a0ecc-121">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="a0ecc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ecc-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0ecc-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a0ecc-123">Name of the resource group.</span></span>

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

### <span data-ttu-id="a0ecc-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a0ecc-124">-ResourceId</span></span>
<span data-ttu-id="a0ecc-125">Ressourcen-ID des verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="a0ecc-125">Resource ID of the managed HSM.</span></span>

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

### <span data-ttu-id="a0ecc-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0ecc-126">-Tag</span></span>
<span data-ttu-id="a0ecc-127">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="a0ecc-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="a0ecc-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0ecc-128">-Confirm</span></span>
<span data-ttu-id="a0ecc-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0ecc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0ecc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0ecc-130">-WhatIf</span></span>
<span data-ttu-id="a0ecc-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ecc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0ecc-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0ecc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0ecc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ecc-133">CommonParameters</span></span>
<span data-ttu-id="a0ecc-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0ecc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ecc-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0ecc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ecc-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0ecc-136">INPUTS</span></span>

### <span data-ttu-id="a0ecc-137">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a0ecc-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="a0ecc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a0ecc-138">System.String</span></span>

### <span data-ttu-id="a0ecc-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a0ecc-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a0ecc-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0ecc-140">OUTPUTS</span></span>

### <span data-ttu-id="a0ecc-141">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a0ecc-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="a0ecc-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0ecc-142">NOTES</span></span>

## <span data-ttu-id="a0ecc-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0ecc-143">RELATED LINKS</span></span>

[<span data-ttu-id="a0ecc-144">Neu – AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a0ecc-144">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="a0ecc-145">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a0ecc-145">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="a0ecc-146">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a0ecc-146">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)