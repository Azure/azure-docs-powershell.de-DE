---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 824b3226b29ba381b9ed963bf6a21f4691c17733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662946"
---
# <span data-ttu-id="a589f-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a589f-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="a589f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a589f-102">SYNOPSIS</span></span>
<span data-ttu-id="a589f-103">Entfernt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="a589f-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a589f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a589f-104">SYNTAX</span></span>

### <span data-ttu-id="a589f-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a589f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a589f-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a589f-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a589f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a589f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a589f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a589f-108">DESCRIPTION</span></span>
<span data-ttu-id="a589f-109">Das Remove-AzureRmContainerRegistryReplication-Cmdlet entfernt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="a589f-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="a589f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a589f-110">EXAMPLES</span></span>

### <span data-ttu-id="a589f-111">Beispiel 1: entfernt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="a589f-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="a589f-112">Entfernt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="a589f-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="a589f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a589f-113">PARAMETERS</span></span>

### <span data-ttu-id="a589f-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a589f-114">-Confirm</span></span>
<span data-ttu-id="a589f-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a589f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a589f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a589f-116">-DefaultProfile</span></span>
<span data-ttu-id="a589f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a589f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a589f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a589f-118">-Name</span></span>
<span data-ttu-id="a589f-119">Name der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="a589f-119">Container Registry Replication Name.</span></span>
<span data-ttu-id="a589f-120">Standardmäßig auf den Namen des Standorts.</span><span class="sxs-lookup"><span data-stu-id="a589f-120">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a589f-121">-Registryname</span><span class="sxs-lookup"><span data-stu-id="a589f-121">-RegistryName</span></span>
<span data-ttu-id="a589f-122">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="a589f-122">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a589f-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="a589f-123">-Replicatoin</span></span>
<span data-ttu-id="a589f-124">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="a589f-124">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a589f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a589f-125">-ResourceGroupName</span></span>
<span data-ttu-id="a589f-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a589f-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a589f-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a589f-127">-ResourceId</span></span>
<span data-ttu-id="a589f-128">Die Ressourcen-ID der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="a589f-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="a589f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a589f-129">-WhatIf</span></span>
<span data-ttu-id="a589f-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a589f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a589f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a589f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a589f-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a589f-132">-PassThru</span></span>
<span data-ttu-id="a589f-133">Gibt an, dass dieses Cmdlet "true" zurückgibt, wenn die Entfernung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a589f-133">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a589f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a589f-134">CommonParameters</span></span>
<span data-ttu-id="a589f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a589f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a589f-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a589f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a589f-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a589f-137">INPUTS</span></span>

### <span data-ttu-id="a589f-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a589f-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="a589f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a589f-139">System.String</span></span>

## <span data-ttu-id="a589f-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a589f-140">OUTPUTS</span></span>

### <span data-ttu-id="a589f-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="a589f-141">System.Object</span></span>

## <span data-ttu-id="a589f-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a589f-142">NOTES</span></span>

## <span data-ttu-id="a589f-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a589f-143">RELATED LINKS</span></span>

[<span data-ttu-id="a589f-144">Neu – AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a589f-144">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="a589f-145">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a589f-145">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

