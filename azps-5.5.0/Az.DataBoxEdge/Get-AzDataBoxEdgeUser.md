---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: cc03472aa71665a8612e17bfce6365a255f929bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162132"
---
# <span data-ttu-id="85482-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="85482-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="85482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85482-102">SYNOPSIS</span></span>
<span data-ttu-id="85482-103">Ruft die konfigurierten Benutzer für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="85482-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="85482-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85482-104">SYNTAX</span></span>

### <span data-ttu-id="85482-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="85482-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85482-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85482-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85482-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="85482-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85482-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85482-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="85482-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85482-109">DESCRIPTION</span></span>
<span data-ttu-id="85482-110">Das **Cmdlet "Get-AzDataBoxEdgeUser"** listet die Benutzer auf, die für ein Datenfeld-Edgegerät konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="85482-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="85482-111">Sie können den Namen in Parametern erwähnen, um Details zu einem bestimmten Benutzer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="85482-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="85482-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85482-112">EXAMPLES</span></span>

### <span data-ttu-id="85482-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85482-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="85482-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85482-114">PARAMETERS</span></span>

### <span data-ttu-id="85482-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85482-115">-DefaultProfile</span></span>
<span data-ttu-id="85482-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85482-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85482-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="85482-117">-DeviceName</span></span>
<span data-ttu-id="85482-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="85482-118">Device Name</span></span>

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

### <span data-ttu-id="85482-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="85482-119">-DeviceObject</span></span>
<span data-ttu-id="85482-120">Geben Sie bitte ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="85482-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="85482-121">-Name</span><span class="sxs-lookup"><span data-stu-id="85482-121">-Name</span></span>
<span data-ttu-id="85482-122">Benutzername</span><span class="sxs-lookup"><span data-stu-id="85482-122">Username</span></span>

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

### <span data-ttu-id="85482-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85482-123">-ResourceGroupName</span></span>
<span data-ttu-id="85482-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="85482-124">Resource Group Name</span></span>

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

### <span data-ttu-id="85482-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85482-125">-ResourceId</span></span>
<span data-ttu-id="85482-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="85482-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="85482-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85482-127">CommonParameters</span></span>
<span data-ttu-id="85482-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85482-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85482-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85482-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85482-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85482-130">INPUTS</span></span>

### <span data-ttu-id="85482-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="85482-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="85482-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85482-132">OUTPUTS</span></span>

### <span data-ttu-id="85482-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="85482-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="85482-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85482-134">NOTES</span></span>

## <span data-ttu-id="85482-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85482-135">RELATED LINKS</span></span>
