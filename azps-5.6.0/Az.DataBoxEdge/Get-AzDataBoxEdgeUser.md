---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: 7f2d4f7461bebd0797e779ad57295e8f45e8de4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942907"
---
# <span data-ttu-id="a18c2-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a18c2-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="a18c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a18c2-102">SYNOPSIS</span></span>
<span data-ttu-id="a18c2-103">Ruft die konfigurierten Benutzer für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="a18c2-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="a18c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a18c2-104">SYNTAX</span></span>

### <span data-ttu-id="a18c2-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a18c2-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18c2-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a18c2-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18c2-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a18c2-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18c2-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a18c2-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a18c2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a18c2-109">DESCRIPTION</span></span>
<span data-ttu-id="a18c2-110">Im **Cmdlet Get-AzDataBoxEdgeUser** werden die Benutzer aufgeführt, die für ein Data Box Edge-Gerät konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="a18c2-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="a18c2-111">Sie können den Namen in Parametern erwähnen, um Details zu einem bestimmten Benutzer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a18c2-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="a18c2-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a18c2-112">EXAMPLES</span></span>

### <span data-ttu-id="a18c2-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a18c2-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="a18c2-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a18c2-114">PARAMETERS</span></span>

### <span data-ttu-id="a18c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a18c2-115">-DefaultProfile</span></span>
<span data-ttu-id="a18c2-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a18c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a18c2-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a18c2-117">-DeviceName</span></span>
<span data-ttu-id="a18c2-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="a18c2-118">Device Name</span></span>

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

### <span data-ttu-id="a18c2-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a18c2-119">-DeviceObject</span></span>
<span data-ttu-id="a18c2-120">Bitte geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="a18c2-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="a18c2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a18c2-121">-Name</span></span>
<span data-ttu-id="a18c2-122">Benutzername</span><span class="sxs-lookup"><span data-stu-id="a18c2-122">Username</span></span>

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

### <span data-ttu-id="a18c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a18c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="a18c2-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="a18c2-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a18c2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a18c2-125">-ResourceId</span></span>
<span data-ttu-id="a18c2-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a18c2-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="a18c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18c2-127">CommonParameters</span></span>
<span data-ttu-id="a18c2-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a18c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18c2-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a18c2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18c2-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a18c2-130">INPUTS</span></span>

### <span data-ttu-id="a18c2-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a18c2-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a18c2-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a18c2-132">OUTPUTS</span></span>

### <span data-ttu-id="a18c2-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a18c2-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="a18c2-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a18c2-134">NOTES</span></span>

## <span data-ttu-id="a18c2-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a18c2-135">RELATED LINKS</span></span>
