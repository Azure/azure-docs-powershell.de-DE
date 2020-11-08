---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177313"
---
# <span data-ttu-id="60018-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="60018-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="60018-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60018-102">SYNOPSIS</span></span>
<span data-ttu-id="60018-103">Löschen eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="60018-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="60018-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60018-104">SYNTAX</span></span>

### <span data-ttu-id="60018-105">GroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="60018-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60018-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60018-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60018-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60018-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60018-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60018-108">DESCRIPTION</span></span>
<span data-ttu-id="60018-109">Löschen eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="60018-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="60018-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60018-110">EXAMPLES</span></span>

### <span data-ttu-id="60018-111">Löschen eines vorhandenen verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="60018-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="60018-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="60018-112">PARAMETERS</span></span>

### <span data-ttu-id="60018-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60018-113">-AsJob</span></span>
<span data-ttu-id="60018-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="60018-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60018-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60018-115">-DefaultProfile</span></span>
<span data-ttu-id="60018-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60018-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60018-117">-Force</span><span class="sxs-lookup"><span data-stu-id="60018-117">-Force</span></span>
<span data-ttu-id="60018-118">Entfernen eines verwalteten Kubernetes-Clusters ohne Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="60018-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="60018-119">-ID</span><span class="sxs-lookup"><span data-stu-id="60018-119">-Id</span></span>
<span data-ttu-id="60018-120">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="60018-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60018-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="60018-121">-InputObject</span></span>
<span data-ttu-id="60018-122">Ein PSKubernetesCluster-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="60018-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60018-123">-Name</span><span class="sxs-lookup"><span data-stu-id="60018-123">-Name</span></span>
<span data-ttu-id="60018-124">Name Ihres verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="60018-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60018-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60018-125">-PassThru</span></span>
<span data-ttu-id="60018-126">Gibt WAHR zurück, wenn der Löschvorgang erfolgreich war</span><span class="sxs-lookup"><span data-stu-id="60018-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="60018-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60018-127">-ResourceGroupName</span></span>
<span data-ttu-id="60018-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="60018-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60018-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="60018-129">-Confirm</span></span>
<span data-ttu-id="60018-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60018-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60018-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60018-131">-WhatIf</span></span>
<span data-ttu-id="60018-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60018-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60018-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60018-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60018-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60018-134">CommonParameters</span></span>
<span data-ttu-id="60018-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60018-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60018-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60018-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60018-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60018-137">INPUTS</span></span>

### <span data-ttu-id="60018-138">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="60018-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="60018-139">System. String</span><span class="sxs-lookup"><span data-stu-id="60018-139">System.String</span></span>

## <span data-ttu-id="60018-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60018-140">OUTPUTS</span></span>

### <span data-ttu-id="60018-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60018-141">System.Boolean</span></span>

## <span data-ttu-id="60018-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="60018-142">NOTES</span></span>

## <span data-ttu-id="60018-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60018-143">RELATED LINKS</span></span>
