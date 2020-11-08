---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3e78e302aafb3e59293f04ade7035e5b4ebbd84c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172983"
---
# <span data-ttu-id="c6339-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="c6339-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="c6339-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6339-102">SYNOPSIS</span></span>
<span data-ttu-id="c6339-103">Aktualisiert das Tag für den angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="c6339-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="c6339-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6339-104">SYNTAX</span></span>

### <span data-ttu-id="c6339-105">ClusterPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6339-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6339-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6339-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6339-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c6339-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6339-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6339-108">DESCRIPTION</span></span>
<span data-ttu-id="c6339-109">Das Set-AzEventHubCluster-Cmdlet aktualisiert die Tags des angegebenen Clusters.</span><span class="sxs-lookup"><span data-stu-id="c6339-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="c6339-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6339-110">EXAMPLES</span></span>

### <span data-ttu-id="c6339-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6339-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Tag @{"ClusterTag3" = "Tag3"; "ClusterTag4" = "Tag4";}

Id        : /subscriptions/{SubID}/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag3, Tag3], [ClusterTag4, Tag4]}
```

<span data-ttu-id="c6339-112">Aktualisiert Tags des angegebenen Clusters.</span><span class="sxs-lookup"><span data-stu-id="c6339-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="c6339-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6339-113">PARAMETERS</span></span>

### <span data-ttu-id="c6339-114">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="c6339-114">-Capacity</span></span>
<span data-ttu-id="c6339-115">Cluster Kapazität (Cu), curerntrly, zulässiger Wert = 1</span><span class="sxs-lookup"><span data-stu-id="c6339-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6339-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6339-116">-DefaultProfile</span></span>
<span data-ttu-id="c6339-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6339-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6339-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c6339-118">-InputObject</span></span>
<span data-ttu-id="c6339-119">Cluster Name</span><span class="sxs-lookup"><span data-stu-id="c6339-119">Cluster Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6339-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="c6339-120">-Location</span></span>
<span data-ttu-id="c6339-121">Speicherort des Clusters</span><span class="sxs-lookup"><span data-stu-id="c6339-121">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6339-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c6339-122">-Name</span></span>
<span data-ttu-id="c6339-123">Cluster Name</span><span class="sxs-lookup"><span data-stu-id="c6339-123">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6339-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6339-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6339-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="c6339-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6339-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c6339-126">-ResourceId</span></span>
<span data-ttu-id="c6339-127">Ressourcen-ID des Clusters</span><span class="sxs-lookup"><span data-stu-id="c6339-127">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6339-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6339-128">-Tag</span></span>
<span data-ttu-id="c6339-129">Hashtables, die das Ressourcen-Tag für Cluster darstellen</span><span class="sxs-lookup"><span data-stu-id="c6339-129">Hashtables which represents resource Tag for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6339-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c6339-130">-Confirm</span></span>
<span data-ttu-id="c6339-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6339-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6339-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6339-132">-WhatIf</span></span>
<span data-ttu-id="c6339-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6339-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6339-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6339-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6339-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6339-135">CommonParameters</span></span>
<span data-ttu-id="c6339-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6339-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6339-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6339-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6339-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6339-138">INPUTS</span></span>

### <span data-ttu-id="c6339-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c6339-139">System.String</span></span>

### <span data-ttu-id="c6339-140">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c6339-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c6339-141">Microsoft. Azure. Commands. EventHub. Models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="c6339-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="c6339-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c6339-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c6339-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6339-143">OUTPUTS</span></span>

### <span data-ttu-id="c6339-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="c6339-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="c6339-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6339-145">NOTES</span></span>

## <span data-ttu-id="c6339-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6339-146">RELATED LINKS</span></span>
