---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/remove-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
ms.openlocfilehash: 1843322f702f8c43f97f1cf64c9d9f5b92d419bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500657"
---
# <span data-ttu-id="5dc8f-101">Remove-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="5dc8f-101">Remove-AzureRmAks</span></span>

## <span data-ttu-id="5dc8f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5dc8f-102">SYNOPSIS</span></span>
<span data-ttu-id="5dc8f-103">Löschen eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="5dc8f-103">Delete a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dc8f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dc8f-104">SYNTAX</span></span>

### <span data-ttu-id="5dc8f-105">GroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5dc8f-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dc8f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dc8f-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dc8f-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dc8f-107">IdParameterSet</span></span>
```
Remove-AzureRmAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dc8f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5dc8f-108">DESCRIPTION</span></span>
<span data-ttu-id="5dc8f-109">Löschen eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="5dc8f-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="5dc8f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5dc8f-110">EXAMPLES</span></span>

### <span data-ttu-id="5dc8f-111">Löschen eines vorhandenen verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="5dc8f-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="5dc8f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5dc8f-112">PARAMETERS</span></span>

### <span data-ttu-id="5dc8f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5dc8f-113">-AsJob</span></span>
<span data-ttu-id="5dc8f-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5dc8f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5dc8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dc8f-115">-DefaultProfile</span></span>
<span data-ttu-id="5dc8f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5dc8f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dc8f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5dc8f-117">-Force</span></span>
<span data-ttu-id="5dc8f-118">Entfernen eines verwalteten Kubernetes-Clusters ohne Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="5dc8f-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="5dc8f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="5dc8f-119">-Id</span></span>
<span data-ttu-id="5dc8f-120">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="5dc8f-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dc8f-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5dc8f-121">-InputObject</span></span>
<span data-ttu-id="5dc8f-122">Ein PSKubernetesCluster-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5dc8f-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dc8f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5dc8f-123">-Name</span></span>
<span data-ttu-id="5dc8f-124">Name Ihres verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="5dc8f-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dc8f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5dc8f-125">-PassThru</span></span>
<span data-ttu-id="5dc8f-126">Gibt WAHR zurück, wenn der Löschvorgang erfolgreich war</span><span class="sxs-lookup"><span data-stu-id="5dc8f-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="5dc8f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dc8f-127">-ResourceGroupName</span></span>
<span data-ttu-id="5dc8f-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="5dc8f-128">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dc8f-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5dc8f-129">-Confirm</span></span>
<span data-ttu-id="5dc8f-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5dc8f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dc8f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dc8f-131">-WhatIf</span></span>
<span data-ttu-id="5dc8f-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5dc8f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dc8f-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5dc8f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dc8f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dc8f-134">CommonParameters</span></span>
<span data-ttu-id="5dc8f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dc8f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dc8f-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dc8f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dc8f-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5dc8f-137">INPUTS</span></span>

### <span data-ttu-id="5dc8f-138">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="5dc8f-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="5dc8f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5dc8f-139">System.String</span></span>

## <span data-ttu-id="5dc8f-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5dc8f-140">OUTPUTS</span></span>

### <span data-ttu-id="5dc8f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5dc8f-141">System.Boolean</span></span>

## <span data-ttu-id="5dc8f-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="5dc8f-142">NOTES</span></span>

## <span data-ttu-id="5dc8f-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5dc8f-143">RELATED LINKS</span></span>
