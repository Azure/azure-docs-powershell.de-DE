---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 31170e24e88f6ce25c9fd344d254189eeeae64f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662950"
---
# <span data-ttu-id="ec9d0-101">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ec9d0-101">New-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="ec9d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec9d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ec9d0-103">Erstellt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-103">Creates a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec9d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec9d0-104">SYNTAX</span></span>

### <span data-ttu-id="ec9d0-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec9d0-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 -Location <String> [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec9d0-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec9d0-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec9d0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec9d0-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec9d0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec9d0-108">DESCRIPTION</span></span>
<span data-ttu-id="ec9d0-109">Das New-AzureRmContainerRegistryReplication-Cmdlet erstellt eine neue Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-109">The New-AzureRmContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="ec9d0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec9d0-110">EXAMPLES</span></span>

### <span data-ttu-id="ec9d0-111">Beispiel 1: Erstellen einer neuen Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="ec9d0-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="ec9d0-112">Erstellen Sie eine neue Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="ec9d0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec9d0-113">PARAMETERS</span></span>

### <span data-ttu-id="ec9d0-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ec9d0-114">-Confirm</span></span>
<span data-ttu-id="ec9d0-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec9d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec9d0-116">-DefaultProfile</span></span>
<span data-ttu-id="ec9d0-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec9d0-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="ec9d0-118">-Location</span></span>
<span data-ttu-id="ec9d0-119">Speicherort der Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-119">Container Registry Location.</span></span>
<span data-ttu-id="ec9d0-120">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-120">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9d0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ec9d0-121">-Name</span></span>
<span data-ttu-id="ec9d0-122">Name der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="ec9d0-122">Container Registry Replication Name.</span></span>
<span data-ttu-id="ec9d0-123">Standardmäßig auf den Namen des Standorts.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-123">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9d0-124">-Registry</span><span class="sxs-lookup"><span data-stu-id="ec9d0-124">-Registry</span></span>
<span data-ttu-id="ec9d0-125">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-125">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9d0-126">-Registryname</span><span class="sxs-lookup"><span data-stu-id="ec9d0-126">-RegistryName</span></span>
<span data-ttu-id="ec9d0-127">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="ec9d0-127">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9d0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec9d0-128">-ResourceGroupName</span></span>
<span data-ttu-id="ec9d0-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9d0-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ec9d0-130">-ResourceId</span></span>
<span data-ttu-id="ec9d0-131">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="ec9d0-131">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec9d0-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec9d0-132">-Tag</span></span>
<span data-ttu-id="ec9d0-133">Container-Registrierungs Tags.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-133">Container Registry Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9d0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec9d0-134">-WhatIf</span></span>
<span data-ttu-id="ec9d0-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec9d0-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec9d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec9d0-137">CommonParameters</span></span>
<span data-ttu-id="ec9d0-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec9d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec9d0-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec9d0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec9d0-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec9d0-140">INPUTS</span></span>

### <span data-ttu-id="ec9d0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ec9d0-141">System.String</span></span>

## <span data-ttu-id="ec9d0-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec9d0-142">OUTPUTS</span></span>

### <span data-ttu-id="ec9d0-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ec9d0-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="ec9d0-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec9d0-144">NOTES</span></span>

## <span data-ttu-id="ec9d0-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec9d0-145">RELATED LINKS</span></span>

[<span data-ttu-id="ec9d0-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ec9d0-146">Get-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="ec9d0-147">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ec9d0-147">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
