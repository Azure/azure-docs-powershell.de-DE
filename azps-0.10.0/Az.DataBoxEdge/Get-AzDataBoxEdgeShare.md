---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 9bcc19d29bf372aaa0b1c59e23f53e80edde4d17
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844131"
---
# <span data-ttu-id="0f6da-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="0f6da-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="0f6da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f6da-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6da-103">Ruft die verfügbaren Freigaben für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="0f6da-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="0f6da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f6da-104">SYNTAX</span></span>

### <span data-ttu-id="0f6da-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f6da-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f6da-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f6da-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f6da-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f6da-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f6da-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f6da-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="0f6da-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f6da-109">DESCRIPTION</span></span>
<span data-ttu-id="0f6da-110">Das Cmdlet " **Get-AzDataBoxEdgeShare** " Ruft die verfügbaren Freigaben für ein Daten Feld-Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="0f6da-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="0f6da-111">Wenn Name angegeben wird, wird die Freigabe nach Namen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0f6da-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="0f6da-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f6da-112">EXAMPLES</span></span>

### <span data-ttu-id="0f6da-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f6da-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="0f6da-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f6da-114">PARAMETERS</span></span>

### <span data-ttu-id="0f6da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f6da-115">-DefaultProfile</span></span>
<span data-ttu-id="0f6da-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0f6da-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f6da-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0f6da-117">-DeviceName</span></span>
<span data-ttu-id="0f6da-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="0f6da-118">Device Name</span></span>

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

### <span data-ttu-id="0f6da-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="0f6da-119">-DeviceObject</span></span>
<span data-ttu-id="0f6da-120">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="0f6da-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="0f6da-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0f6da-121">-Name</span></span>
<span data-ttu-id="0f6da-122">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="0f6da-122">Resource Name</span></span>

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

### <span data-ttu-id="0f6da-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f6da-123">-ResourceGroupName</span></span>
<span data-ttu-id="0f6da-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0f6da-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0f6da-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0f6da-125">-ResourceId</span></span>
<span data-ttu-id="0f6da-126">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="0f6da-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="0f6da-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6da-127">CommonParameters</span></span>
<span data-ttu-id="0f6da-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f6da-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6da-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f6da-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6da-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f6da-130">INPUTS</span></span>

### <span data-ttu-id="0f6da-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0f6da-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="0f6da-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f6da-132">OUTPUTS</span></span>

### <span data-ttu-id="0f6da-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="0f6da-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="0f6da-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f6da-134">NOTES</span></span>

## <span data-ttu-id="0f6da-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f6da-135">RELATED LINKS</span></span>
