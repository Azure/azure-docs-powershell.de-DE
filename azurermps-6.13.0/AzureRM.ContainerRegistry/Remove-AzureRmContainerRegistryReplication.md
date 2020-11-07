---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 7dfb080ae20c583467add8ce298b03199a4f89dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664081"
---
# <span data-ttu-id="c2864-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c2864-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="c2864-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2864-102">SYNOPSIS</span></span>
<span data-ttu-id="c2864-103">Entfernt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="c2864-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2864-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2864-104">SYNTAX</span></span>

### <span data-ttu-id="c2864-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2864-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2864-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2864-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2864-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2864-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2864-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2864-108">DESCRIPTION</span></span>
<span data-ttu-id="c2864-109">Das Remove-AzureRmContainerRegistryReplication-Cmdlet entfernt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="c2864-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="c2864-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2864-110">EXAMPLES</span></span>

### <span data-ttu-id="c2864-111">Beispiel 1: entfernt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="c2864-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="c2864-112">Entfernt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="c2864-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="c2864-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2864-113">PARAMETERS</span></span>

### <span data-ttu-id="c2864-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2864-114">-DefaultProfile</span></span>
<span data-ttu-id="c2864-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2864-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2864-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c2864-116">-Name</span></span>
<span data-ttu-id="c2864-117">Name der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="c2864-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="c2864-118">Standardmäßig auf den Namen des Standorts.</span><span class="sxs-lookup"><span data-stu-id="c2864-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2864-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2864-119">-PassThru</span></span>
<span data-ttu-id="c2864-120">Gibt an, dass dieses Cmdlet "true" zurückgibt, wenn die Entfernung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c2864-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="c2864-121">-Registryname</span><span class="sxs-lookup"><span data-stu-id="c2864-121">-RegistryName</span></span>
<span data-ttu-id="c2864-122">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="c2864-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2864-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="c2864-123">-Replicatoin</span></span>
<span data-ttu-id="c2864-124">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c2864-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2864-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2864-125">-ResourceGroupName</span></span>
<span data-ttu-id="c2864-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2864-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2864-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c2864-127">-ResourceId</span></span>
<span data-ttu-id="c2864-128">Die Ressourcen-ID der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="c2864-128">The container registry replication resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2864-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2864-129">-Confirm</span></span>
<span data-ttu-id="c2864-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2864-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2864-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2864-131">-WhatIf</span></span>
<span data-ttu-id="c2864-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2864-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2864-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2864-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2864-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2864-134">CommonParameters</span></span>
<span data-ttu-id="c2864-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2864-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2864-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2864-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2864-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2864-137">INPUTS</span></span>

### <span data-ttu-id="c2864-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c2864-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="c2864-139">Parameter: Replicatoin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c2864-139">Parameters: Replicatoin (ByValue)</span></span>

### <span data-ttu-id="c2864-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c2864-140">System.String</span></span>

## <span data-ttu-id="c2864-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2864-141">OUTPUTS</span></span>

### <span data-ttu-id="c2864-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2864-142">System.Boolean</span></span>

## <span data-ttu-id="c2864-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2864-143">NOTES</span></span>

## <span data-ttu-id="c2864-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2864-144">RELATED LINKS</span></span>

[<span data-ttu-id="c2864-145">Neu – AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c2864-145">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="c2864-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c2864-146">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

