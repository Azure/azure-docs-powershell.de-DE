---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178194"
---
# <span data-ttu-id="d34ab-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="d34ab-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="d34ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d34ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d34ab-103">Ruft die auf einem Gerät geplanten Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="d34ab-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="d34ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d34ab-104">SYNTAX</span></span>

### <span data-ttu-id="d34ab-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d34ab-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d34ab-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="d34ab-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d34ab-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d34ab-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="d34ab-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d34ab-108">DESCRIPTION</span></span>
<span data-ttu-id="d34ab-109">Das Cmdlet " **Get-AzStackEdgeJob** " Ruft die aktiven Aufträge auf einem Stack-Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="d34ab-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="d34ab-110">Sie können den Parameter Name erwähnen, um Details zu einem bestimmten Job abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d34ab-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="d34ab-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d34ab-111">EXAMPLES</span></span>

### <span data-ttu-id="d34ab-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d34ab-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="d34ab-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d34ab-113">PARAMETERS</span></span>

### <span data-ttu-id="d34ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d34ab-114">-DefaultProfile</span></span>
<span data-ttu-id="d34ab-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d34ab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d34ab-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d34ab-116">-DeviceName</span></span>
<span data-ttu-id="d34ab-117">Name des Geräts</span><span class="sxs-lookup"><span data-stu-id="d34ab-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d34ab-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d34ab-118">-DeviceObject</span></span>
<span data-ttu-id="d34ab-119">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="d34ab-119">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d34ab-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d34ab-120">-Name</span></span>
<span data-ttu-id="d34ab-121">Name des Auftrags, in der Regel eine GUID</span><span class="sxs-lookup"><span data-stu-id="d34ab-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: Job

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d34ab-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d34ab-122">-ResourceGroupName</span></span>
<span data-ttu-id="d34ab-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="d34ab-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d34ab-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d34ab-124">-ResourceId</span></span>
<span data-ttu-id="d34ab-125">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="d34ab-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d34ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34ab-126">CommonParameters</span></span>
<span data-ttu-id="d34ab-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d34ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34ab-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d34ab-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34ab-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d34ab-129">INPUTS</span></span>

### <span data-ttu-id="d34ab-130">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d34ab-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="d34ab-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d34ab-131">OUTPUTS</span></span>

### <span data-ttu-id="d34ab-132">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="d34ab-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="d34ab-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="d34ab-133">NOTES</span></span>

## <span data-ttu-id="d34ab-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d34ab-134">RELATED LINKS</span></span>
