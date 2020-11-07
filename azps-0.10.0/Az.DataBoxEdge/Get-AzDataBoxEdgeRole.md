---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 0af708265a66ecf05bfe4eb5de37d7b81a21aa3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844132"
---
# <span data-ttu-id="64abc-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="64abc-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="64abc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64abc-102">SYNOPSIS</span></span>
<span data-ttu-id="64abc-103">Ruft die verfügbaren Rollen für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="64abc-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="64abc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64abc-104">SYNTAX</span></span>

### <span data-ttu-id="64abc-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="64abc-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64abc-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64abc-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64abc-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64abc-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64abc-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64abc-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="64abc-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64abc-109">DESCRIPTION</span></span>
<span data-ttu-id="64abc-110">Das Cmdlet " **Get-AzDataBoxEdgeRole** " Ruft die verfügbaren Rollen für ein Edge-Gerät für Datenfelder ab.</span><span class="sxs-lookup"><span data-stu-id="64abc-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="64abc-111">Sie können den Parameter Name erwähnen, um die Details einer bestimmten Rolle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="64abc-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="64abc-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64abc-112">EXAMPLES</span></span>

### <span data-ttu-id="64abc-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64abc-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="64abc-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="64abc-114">PARAMETERS</span></span>

### <span data-ttu-id="64abc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64abc-115">-DefaultProfile</span></span>
<span data-ttu-id="64abc-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64abc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64abc-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="64abc-117">-DeviceName</span></span>
<span data-ttu-id="64abc-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="64abc-118">Device Name</span></span>

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

### <span data-ttu-id="64abc-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="64abc-119">-DeviceObject</span></span>
<span data-ttu-id="64abc-120">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="64abc-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="64abc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="64abc-121">-Name</span></span>
<span data-ttu-id="64abc-122">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="64abc-122">Resource Name</span></span>

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

### <span data-ttu-id="64abc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64abc-123">-ResourceGroupName</span></span>
<span data-ttu-id="64abc-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="64abc-124">Resource Group Name</span></span>

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

### <span data-ttu-id="64abc-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="64abc-125">-ResourceId</span></span>
<span data-ttu-id="64abc-126">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="64abc-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="64abc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64abc-127">CommonParameters</span></span>
<span data-ttu-id="64abc-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64abc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64abc-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64abc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64abc-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64abc-130">INPUTS</span></span>

### <span data-ttu-id="64abc-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="64abc-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="64abc-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64abc-132">OUTPUTS</span></span>

### <span data-ttu-id="64abc-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="64abc-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="64abc-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="64abc-134">NOTES</span></span>

## <span data-ttu-id="64abc-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64abc-135">RELATED LINKS</span></span>
