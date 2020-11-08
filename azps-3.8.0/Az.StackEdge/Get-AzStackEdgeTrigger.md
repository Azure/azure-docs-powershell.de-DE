---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995755"
---
# <span data-ttu-id="fa4f4-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="fa4f4-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="fa4f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="fa4f4-103">Abrufen der auf einem Gerät konfigurierten Trigger</span><span class="sxs-lookup"><span data-stu-id="fa4f4-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="fa4f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa4f4-104">SYNTAX</span></span>

### <span data-ttu-id="fa4f4-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa4f4-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa4f4-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa4f4-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa4f4-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa4f4-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa4f4-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa4f4-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="fa4f4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa4f4-109">DESCRIPTION</span></span>
<span data-ttu-id="fa4f4-110">Das Cmdlet " **Get-AzStackEdgeTriger** " Ruft die Trigger für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="fa4f4-111">Sie können den Namen als Parameter im Cmdlet angeben, um die Details eines bestimmten Triggers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="fa4f4-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa4f4-112">EXAMPLES</span></span>

### <span data-ttu-id="fa4f4-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fa4f4-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="fa4f4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa4f4-114">PARAMETERS</span></span>

### <span data-ttu-id="fa4f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa4f4-115">-DefaultProfile</span></span>
<span data-ttu-id="fa4f4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa4f4-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fa4f4-117">-DeviceName</span></span>
<span data-ttu-id="fa4f4-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="fa4f4-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa4f4-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="fa4f4-119">-DeviceObject</span></span>
<span data-ttu-id="fa4f4-120">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="fa4f4-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa4f4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fa4f4-121">-Name</span></span>
<span data-ttu-id="fa4f4-122">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="fa4f4-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa4f4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa4f4-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa4f4-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="fa4f4-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa4f4-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fa4f4-125">-ResourceId</span></span>
<span data-ttu-id="fa4f4-126">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="fa4f4-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa4f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa4f4-127">CommonParameters</span></span>
<span data-ttu-id="fa4f4-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa4f4-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa4f4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa4f4-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa4f4-130">INPUTS</span></span>

### <span data-ttu-id="fa4f4-131">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="fa4f4-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="fa4f4-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa4f4-132">OUTPUTS</span></span>

### <span data-ttu-id="fa4f4-133">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="fa4f4-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="fa4f4-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa4f4-134">NOTES</span></span>

## <span data-ttu-id="fa4f4-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa4f4-135">RELATED LINKS</span></span>
