---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004564"
---
# <span data-ttu-id="3b7e9-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="3b7e9-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="3b7e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b7e9-102">SYNOPSIS</span></span>
<span data-ttu-id="3b7e9-103">Erstellen Sie einen neuen Azure-Bereiche-Controller.</span><span class="sxs-lookup"><span data-stu-id="3b7e9-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="3b7e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b7e9-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b7e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b7e9-105">DESCRIPTION</span></span>
<span data-ttu-id="3b7e9-106">Erstellen Sie einen neuen Azure-Bereiche-Controller.</span><span class="sxs-lookup"><span data-stu-id="3b7e9-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="3b7e9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b7e9-107">EXAMPLES</span></span>

### <span data-ttu-id="3b7e9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3b7e9-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="3b7e9-109">Erstellen Sie einen devSpaceResourceGroup mit dem Namen "Name".</span><span class="sxs-lookup"><span data-stu-id="3b7e9-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="3b7e9-110">Verwenden Sie Clustername Cluster als Ziel für diesen Controller.</span><span class="sxs-lookup"><span data-stu-id="3b7e9-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="3b7e9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b7e9-111">PARAMETERS</span></span>

### <span data-ttu-id="3b7e9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b7e9-112">-AsJob</span></span>
<span data-ttu-id="3b7e9-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3b7e9-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b7e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b7e9-114">-DefaultProfile</span></span>
<span data-ttu-id="3b7e9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b7e9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b7e9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3b7e9-116">-Name</span></span>
<span data-ttu-id="3b7e9-117">Name des Domänencontrollers</span><span class="sxs-lookup"><span data-stu-id="3b7e9-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b7e9-118">-ResourceGroupName</span></span>
<span data-ttu-id="3b7e9-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b7e9-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e9-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b7e9-120">-Tag</span></span>
<span data-ttu-id="3b7e9-121">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b7e9-121">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e9-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="3b7e9-122">-TargetClusterName</span></span>
<span data-ttu-id="3b7e9-123">Name des Ziel Clusters</span><span class="sxs-lookup"><span data-stu-id="3b7e9-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e9-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b7e9-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="3b7e9-125">Name der Ziel Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b7e9-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e9-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b7e9-126">-Confirm</span></span>
<span data-ttu-id="3b7e9-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b7e9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b7e9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b7e9-128">-WhatIf</span></span>
<span data-ttu-id="3b7e9-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b7e9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b7e9-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b7e9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b7e9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b7e9-131">CommonParameters</span></span>
<span data-ttu-id="3b7e9-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b7e9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b7e9-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b7e9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b7e9-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b7e9-134">INPUTS</span></span>

### <span data-ttu-id="3b7e9-135">Keine</span><span class="sxs-lookup"><span data-stu-id="3b7e9-135">None</span></span>

## <span data-ttu-id="3b7e9-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b7e9-136">OUTPUTS</span></span>

### <span data-ttu-id="3b7e9-137">Microsoft. Azure. Commands .Bereiche. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="3b7e9-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="3b7e9-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b7e9-138">NOTES</span></span>

## <span data-ttu-id="3b7e9-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b7e9-139">RELATED LINKS</span></span>
