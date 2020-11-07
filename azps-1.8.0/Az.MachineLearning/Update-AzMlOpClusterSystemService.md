---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
ms.openlocfilehash: 0e673cd74d87cee990130c1fd58b9049eec9ff15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819143"
---
# <span data-ttu-id="5e9e9-101">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="5e9e9-101">Update-AzMlOpClusterSystemService</span></span>

## <span data-ttu-id="5e9e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e9e9-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9e9-103">Startet ein Update für die Systemdienste des Operations Clusters.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-103">Starts an update on the operationalization cluster's system services.</span></span>

## <span data-ttu-id="5e9e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e9e9-104">SYNTAX</span></span>

### <span data-ttu-id="5e9e9-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5e9e9-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e9e9-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="5e9e9-106">StartUpdateWithInputObject</span></span>
```
Update-AzMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e9e9-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="5e9e9-107">StartUpdateWithResourceId</span></span>
```
Update-AzMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e9e9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e9e9-108">DESCRIPTION</span></span>
<span data-ttu-id="5e9e9-109">Die Systemdienste können unabhängig vom Operations Cluster aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="5e9e9-110">Verwenden Sie dieses Cmdlet, um ein Update für die Systemdienste zu starten.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="5e9e9-111">Wenn kein Update verfügbar ist, wird ein Update weiterhin gestartet und wird erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="5e9e9-112">Nach Abschluss des Updates meldet es, wenn es gestartet, abgeschlossen und erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="5e9e9-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e9e9-113">EXAMPLES</span></span>

### <span data-ttu-id="5e9e9-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e9e9-114">Example 1</span></span>
```
PS C:\> Update-AzMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="5e9e9-115">Startet ein Systemdienst Update für den angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="5e9e9-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e9e9-116">PARAMETERS</span></span>

### <span data-ttu-id="5e9e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9e9-117">-DefaultProfile</span></span>
<span data-ttu-id="5e9e9-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e9e9-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e9e9-119">-InputObject</span></span>
<span data-ttu-id="5e9e9-120">Das Clusterobjekt für die Operation</span><span class="sxs-lookup"><span data-stu-id="5e9e9-120">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e9e9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5e9e9-121">-Name</span></span>
<span data-ttu-id="5e9e9-122">Der Name des Clusters für die Cluster Operation.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-122">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9e9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e9e9-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e9e9-124">Der Name der Ressourcengruppe für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9e9-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5e9e9-125">-ResourceId</span></span>
<span data-ttu-id="5e9e9-126">Die Azure-Ressourcen-ID für den Zuordnungs Cluster.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e9e9-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e9e9-127">-Confirm</span></span>
<span data-ttu-id="5e9e9-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e9e9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e9e9-129">-WhatIf</span></span>
<span data-ttu-id="5e9e9-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e9e9-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e9e9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9e9-132">CommonParameters</span></span>
<span data-ttu-id="5e9e9-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e9e9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9e9-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e9e9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9e9-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e9e9-135">INPUTS</span></span>

### <span data-ttu-id="5e9e9-136">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="5e9e9-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="5e9e9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5e9e9-137">System.String</span></span>

## <span data-ttu-id="5e9e9-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e9e9-138">OUTPUTS</span></span>

### <span data-ttu-id="5e9e9-139">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="5e9e9-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="5e9e9-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e9e9-140">NOTES</span></span>

## <span data-ttu-id="5e9e9-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e9e9-141">RELATED LINKS</span></span>
