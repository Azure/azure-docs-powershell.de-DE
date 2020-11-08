---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174043"
---
# <span data-ttu-id="26695-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="26695-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="26695-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26695-102">SYNOPSIS</span></span>
<span data-ttu-id="26695-103">Ruft die verfügbaren Freigaben für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="26695-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="26695-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26695-104">SYNTAX</span></span>

### <span data-ttu-id="26695-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="26695-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26695-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26695-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26695-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="26695-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26695-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26695-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="26695-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26695-109">DESCRIPTION</span></span>
<span data-ttu-id="26695-110">Das Cmdlet " **Get-AzStackEdgeShare** " Ruft die verfügbaren Freigaben für ein Stack-Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="26695-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="26695-111">Wenn Name angegeben wird, wird die Freigabe nach Namen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="26695-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="26695-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26695-112">EXAMPLES</span></span>

### <span data-ttu-id="26695-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="26695-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="26695-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="26695-114">PARAMETERS</span></span>

### <span data-ttu-id="26695-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26695-115">-DefaultProfile</span></span>
<span data-ttu-id="26695-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26695-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26695-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="26695-117">-DeviceName</span></span>
<span data-ttu-id="26695-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="26695-118">Device Name</span></span>

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

### <span data-ttu-id="26695-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="26695-119">-DeviceObject</span></span>
<span data-ttu-id="26695-120">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="26695-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="26695-121">-Name</span><span class="sxs-lookup"><span data-stu-id="26695-121">-Name</span></span>
<span data-ttu-id="26695-122">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="26695-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26695-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26695-123">-ResourceGroupName</span></span>
<span data-ttu-id="26695-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="26695-124">Resource Group Name</span></span>

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

### <span data-ttu-id="26695-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="26695-125">-ResourceId</span></span>
<span data-ttu-id="26695-126">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="26695-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="26695-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26695-127">CommonParameters</span></span>
<span data-ttu-id="26695-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26695-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26695-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26695-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26695-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26695-130">INPUTS</span></span>

### <span data-ttu-id="26695-131">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="26695-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="26695-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26695-132">OUTPUTS</span></span>

### <span data-ttu-id="26695-133">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="26695-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="26695-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="26695-134">NOTES</span></span>

## <span data-ttu-id="26695-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26695-135">RELATED LINKS</span></span>
