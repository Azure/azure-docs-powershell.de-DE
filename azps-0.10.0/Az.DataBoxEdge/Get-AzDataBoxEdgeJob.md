---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
ms.openlocfilehash: 4f5626059e4185e5440e7d5a11346c82ce472bbd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844152"
---
# <span data-ttu-id="8c809-101">Get-AzDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="8c809-101">Get-AzDataBoxEdgeJob</span></span>

## <span data-ttu-id="8c809-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c809-102">SYNOPSIS</span></span>
<span data-ttu-id="8c809-103">Ruft die auf einem Gerät geplanten Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="8c809-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="8c809-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c809-104">SYNTAX</span></span>

### <span data-ttu-id="8c809-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8c809-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c809-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="8c809-106">GetByResourceIdObject</span></span>
```
Get-AzDataBoxEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c809-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c809-107">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="8c809-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c809-108">DESCRIPTION</span></span>
<span data-ttu-id="8c809-109">Das Cmdlet " **Get-AzDataBoxEdgeJob** " Ruft die aktiven Aufträge auf einem Daten Feld-Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="8c809-109">The **Get-AzDataBoxEdgeJob** cmdlet gets the active jobs on a Data Box Edge device.</span></span> <span data-ttu-id="8c809-110">Sie können den Parameter Name erwähnen, um Details zu einem bestimmten Job abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8c809-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="8c809-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c809-111">EXAMPLES</span></span>

### <span data-ttu-id="8c809-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8c809-112">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="8c809-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c809-113">PARAMETERS</span></span>

### <span data-ttu-id="8c809-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c809-114">-DefaultProfile</span></span>
<span data-ttu-id="8c809-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8c809-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c809-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8c809-116">-DeviceName</span></span>
<span data-ttu-id="8c809-117">Name des Geräts</span><span class="sxs-lookup"><span data-stu-id="8c809-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c809-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8c809-118">-DeviceObject</span></span>
<span data-ttu-id="8c809-119">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="8c809-119">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c809-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8c809-120">-Name</span></span>
<span data-ttu-id="8c809-121">Name des Auftrags, in der Regel eine GUID</span><span class="sxs-lookup"><span data-stu-id="8c809-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c809-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c809-122">-ResourceGroupName</span></span>
<span data-ttu-id="8c809-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="8c809-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c809-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8c809-124">-ResourceId</span></span>
<span data-ttu-id="8c809-125">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="8c809-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c809-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c809-126">CommonParameters</span></span>
<span data-ttu-id="8c809-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c809-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c809-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c809-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c809-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c809-129">INPUTS</span></span>

### <span data-ttu-id="8c809-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8c809-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="8c809-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c809-131">OUTPUTS</span></span>

### <span data-ttu-id="8c809-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="8c809-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span></span>

## <span data-ttu-id="8c809-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c809-133">NOTES</span></span>

## <span data-ttu-id="8c809-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c809-134">RELATED LINKS</span></span>
