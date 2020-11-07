---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: 0429eebf0425a950bcf093d7659a2d87b3b661f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651325"
---
# <span data-ttu-id="38320-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="38320-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="38320-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38320-102">SYNOPSIS</span></span>
<span data-ttu-id="38320-103">Erstellen Sie einen neuen Azure-Bereiche-Controller.</span><span class="sxs-lookup"><span data-stu-id="38320-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="38320-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38320-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38320-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38320-105">DESCRIPTION</span></span>
<span data-ttu-id="38320-106">Erstellen Sie einen neuen Azure-Bereiche-Controller.</span><span class="sxs-lookup"><span data-stu-id="38320-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="38320-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38320-107">EXAMPLES</span></span>

### <span data-ttu-id="38320-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="38320-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="38320-109">Erstellen Sie einen devSpaceResourceGroup mit dem Namen "Name".</span><span class="sxs-lookup"><span data-stu-id="38320-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="38320-110">Verwenden Sie Clustername Cluster als Ziel für diesen Controller.</span><span class="sxs-lookup"><span data-stu-id="38320-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="38320-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="38320-111">PARAMETERS</span></span>

### <span data-ttu-id="38320-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38320-112">-AsJob</span></span>
<span data-ttu-id="38320-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="38320-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38320-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38320-114">-DefaultProfile</span></span>
<span data-ttu-id="38320-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38320-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38320-116">-Name</span><span class="sxs-lookup"><span data-stu-id="38320-116">-Name</span></span>
<span data-ttu-id="38320-117">Name des Domänencontrollers</span><span class="sxs-lookup"><span data-stu-id="38320-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="38320-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38320-118">-ResourceGroupName</span></span>
<span data-ttu-id="38320-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="38320-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="38320-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="38320-120">-Tag</span></span>
<span data-ttu-id="38320-121">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="38320-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="38320-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="38320-122">-TargetClusterName</span></span>
<span data-ttu-id="38320-123">Name des Ziel Clusters</span><span class="sxs-lookup"><span data-stu-id="38320-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="38320-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38320-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="38320-125">Name der Ziel Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="38320-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="38320-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="38320-126">-Confirm</span></span>
<span data-ttu-id="38320-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38320-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38320-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38320-128">-WhatIf</span></span>
<span data-ttu-id="38320-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38320-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38320-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38320-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38320-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38320-131">CommonParameters</span></span>
<span data-ttu-id="38320-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38320-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38320-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38320-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38320-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38320-134">INPUTS</span></span>

### <span data-ttu-id="38320-135">Keine</span><span class="sxs-lookup"><span data-stu-id="38320-135">None</span></span>

## <span data-ttu-id="38320-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38320-136">OUTPUTS</span></span>

### <span data-ttu-id="38320-137">Microsoft. Azure. Commands .Bereiche. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="38320-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="38320-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="38320-138">NOTES</span></span>

## <span data-ttu-id="38320-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38320-139">RELATED LINKS</span></span>
