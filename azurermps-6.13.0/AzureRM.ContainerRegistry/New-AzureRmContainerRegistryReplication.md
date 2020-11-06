---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: eaab02fe0e0adbd54bc80b15e6520442d9eb3c11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476157"
---
# <span data-ttu-id="4b1ec-101">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4b1ec-101">New-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="4b1ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b1ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4b1ec-103">Erstellt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-103">Creates a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b1ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b1ec-104">SYNTAX</span></span>

### <span data-ttu-id="4b1ec-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b1ec-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 -Location <String> [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b1ec-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b1ec-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b1ec-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b1ec-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b1ec-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b1ec-108">DESCRIPTION</span></span>
<span data-ttu-id="4b1ec-109">Das New-AzureRmContainerRegistryReplication-Cmdlet erstellt eine neue Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-109">The New-AzureRmContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="4b1ec-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b1ec-110">EXAMPLES</span></span>

### <span data-ttu-id="4b1ec-111">Beispiel 1: Erstellen einer neuen Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="4b1ec-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="4b1ec-112">Erstellen Sie eine neue Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="4b1ec-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b1ec-113">PARAMETERS</span></span>

### <span data-ttu-id="4b1ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b1ec-114">-DefaultProfile</span></span>
<span data-ttu-id="4b1ec-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b1ec-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="4b1ec-116">-Location</span></span>
<span data-ttu-id="4b1ec-117">Speicherort der Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-117">Container Registry Location.</span></span>
<span data-ttu-id="4b1ec-118">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="4b1ec-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4b1ec-119">-Name</span></span>
<span data-ttu-id="4b1ec-120">Name der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="4b1ec-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="4b1ec-121">Standardmäßig auf den Namen des Standorts.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-121">Default to the location name.</span></span>

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

### <span data-ttu-id="4b1ec-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="4b1ec-122">-Registry</span></span>
<span data-ttu-id="4b1ec-123">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="4b1ec-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="4b1ec-124">-RegistryName</span></span>
<span data-ttu-id="4b1ec-125">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="4b1ec-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="4b1ec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b1ec-126">-ResourceGroupName</span></span>
<span data-ttu-id="4b1ec-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="4b1ec-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4b1ec-128">-ResourceId</span></span>
<span data-ttu-id="4b1ec-129">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="4b1ec-129">The container registry resource id</span></span>

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

### <span data-ttu-id="4b1ec-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="4b1ec-130">-Tag</span></span>
<span data-ttu-id="4b1ec-131">Container-Registrierungs Tags.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="4b1ec-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b1ec-132">-Confirm</span></span>
<span data-ttu-id="4b1ec-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b1ec-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b1ec-134">-WhatIf</span></span>
<span data-ttu-id="4b1ec-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b1ec-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b1ec-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b1ec-137">CommonParameters</span></span>
<span data-ttu-id="4b1ec-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b1ec-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b1ec-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b1ec-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b1ec-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b1ec-140">INPUTS</span></span>

### <span data-ttu-id="4b1ec-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4b1ec-141">System.String</span></span>

## <span data-ttu-id="4b1ec-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b1ec-142">OUTPUTS</span></span>

### <span data-ttu-id="4b1ec-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4b1ec-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="4b1ec-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b1ec-144">NOTES</span></span>

## <span data-ttu-id="4b1ec-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b1ec-145">RELATED LINKS</span></span>

[<span data-ttu-id="4b1ec-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4b1ec-146">Get-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="4b1ec-147">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4b1ec-147">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
