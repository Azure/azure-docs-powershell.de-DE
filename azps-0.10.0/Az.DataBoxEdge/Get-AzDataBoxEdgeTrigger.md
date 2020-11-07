---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 96c9b736398cb981dd055d072091aa24af4d3f6c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844124"
---
# <span data-ttu-id="058ac-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="058ac-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="058ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="058ac-102">SYNOPSIS</span></span>
<span data-ttu-id="058ac-103">Abrufen der auf einem Gerät konfigurierten Trigger</span><span class="sxs-lookup"><span data-stu-id="058ac-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="058ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="058ac-104">SYNTAX</span></span>

### <span data-ttu-id="058ac-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="058ac-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="058ac-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="058ac-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="058ac-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="058ac-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="058ac-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="058ac-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="058ac-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="058ac-109">DESCRIPTION</span></span>
<span data-ttu-id="058ac-110">Das Cmdlet " **Get-AzDataBoxEdgeTriger** " Ruft die Trigger für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="058ac-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="058ac-111">Sie können den Namen als Parameter im Cmdlet angeben, um die Details eines bestimmten Triggers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="058ac-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="058ac-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="058ac-112">EXAMPLES</span></span>

### <span data-ttu-id="058ac-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="058ac-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="058ac-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="058ac-114">PARAMETERS</span></span>

### <span data-ttu-id="058ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="058ac-115">-DefaultProfile</span></span>
<span data-ttu-id="058ac-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="058ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="058ac-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="058ac-117">-DeviceName</span></span>
<span data-ttu-id="058ac-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="058ac-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="058ac-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="058ac-119">-DeviceObject</span></span>
<span data-ttu-id="058ac-120">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="058ac-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="058ac-121">-Name</span><span class="sxs-lookup"><span data-stu-id="058ac-121">-Name</span></span>
<span data-ttu-id="058ac-122">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="058ac-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="058ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="058ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="058ac-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="058ac-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="058ac-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="058ac-125">-ResourceId</span></span>
<span data-ttu-id="058ac-126">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="058ac-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="058ac-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="058ac-127">CommonParameters</span></span>
<span data-ttu-id="058ac-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="058ac-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="058ac-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="058ac-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="058ac-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="058ac-130">INPUTS</span></span>

### <span data-ttu-id="058ac-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="058ac-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="058ac-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="058ac-132">OUTPUTS</span></span>

### <span data-ttu-id="058ac-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="058ac-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="058ac-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="058ac-134">NOTES</span></span>

## <span data-ttu-id="058ac-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="058ac-135">RELATED LINKS</span></span>
