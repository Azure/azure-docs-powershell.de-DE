---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: 2f5e310df06650b2c8f2506910c80dbf0ea440bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651826"
---
# <span data-ttu-id="d37ba-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d37ba-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="d37ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d37ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d37ba-103">Erstellt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="d37ba-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="d37ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d37ba-104">SYNTAX</span></span>

### <span data-ttu-id="d37ba-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d37ba-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d37ba-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d37ba-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d37ba-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d37ba-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d37ba-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d37ba-108">DESCRIPTION</span></span>
<span data-ttu-id="d37ba-109">Das New-AzContainerRegistryReplication-Cmdlet erstellt eine neue Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="d37ba-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="d37ba-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d37ba-110">EXAMPLES</span></span>

### <span data-ttu-id="d37ba-111">Beispiel 1: Erstellen einer neuen Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="d37ba-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="d37ba-112">Erstellen Sie eine neue Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="d37ba-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="d37ba-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d37ba-113">PARAMETERS</span></span>

### <span data-ttu-id="d37ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37ba-114">-DefaultProfile</span></span>
<span data-ttu-id="d37ba-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d37ba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d37ba-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="d37ba-116">-Location</span></span>
<span data-ttu-id="d37ba-117">Speicherort der Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="d37ba-117">Container Registry Location.</span></span>
<span data-ttu-id="d37ba-118">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="d37ba-118">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37ba-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d37ba-119">-Name</span></span>
<span data-ttu-id="d37ba-120">Name der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="d37ba-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="d37ba-121">Standardmäßig auf den Namen des Standorts.</span><span class="sxs-lookup"><span data-stu-id="d37ba-121">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37ba-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="d37ba-122">-Registry</span></span>
<span data-ttu-id="d37ba-123">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="d37ba-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37ba-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="d37ba-124">-RegistryName</span></span>
<span data-ttu-id="d37ba-125">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="d37ba-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37ba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d37ba-126">-ResourceGroupName</span></span>
<span data-ttu-id="d37ba-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d37ba-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37ba-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d37ba-128">-ResourceId</span></span>
<span data-ttu-id="d37ba-129">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="d37ba-129">The container registry resource id</span></span>

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

### <span data-ttu-id="d37ba-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="d37ba-130">-Tag</span></span>
<span data-ttu-id="d37ba-131">Container-Registrierungs Tags.</span><span class="sxs-lookup"><span data-stu-id="d37ba-131">Container Registry Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37ba-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d37ba-132">-Confirm</span></span>
<span data-ttu-id="d37ba-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d37ba-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d37ba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37ba-134">-WhatIf</span></span>
<span data-ttu-id="d37ba-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d37ba-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d37ba-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d37ba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d37ba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37ba-137">CommonParameters</span></span>
<span data-ttu-id="d37ba-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37ba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37ba-139">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d37ba-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37ba-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d37ba-140">INPUTS</span></span>

### <span data-ttu-id="d37ba-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d37ba-141">System.String</span></span>

## <span data-ttu-id="d37ba-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d37ba-142">OUTPUTS</span></span>

### <span data-ttu-id="d37ba-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d37ba-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="d37ba-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="d37ba-144">NOTES</span></span>

## <span data-ttu-id="d37ba-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d37ba-145">RELATED LINKS</span></span>

[<span data-ttu-id="d37ba-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d37ba-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="d37ba-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d37ba-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)