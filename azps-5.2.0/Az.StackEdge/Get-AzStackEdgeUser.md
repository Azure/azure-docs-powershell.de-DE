---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294664"
---
# <span data-ttu-id="be559-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="be559-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="be559-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be559-102">SYNOPSIS</span></span>
<span data-ttu-id="be559-103">Ruft die konfigurierten Benutzer für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="be559-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="be559-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be559-104">SYNTAX</span></span>

### <span data-ttu-id="be559-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="be559-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be559-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be559-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be559-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="be559-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be559-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be559-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="be559-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be559-109">DESCRIPTION</span></span>
<span data-ttu-id="be559-110">Im **Cmdlet "Get-AzStackEdgeUser"** werden die Benutzer aufgeführt, die für ein Stack Edge-Gerät konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="be559-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="be559-111">Sie können den Namen in Parametern erwähnen, um Details zu einem bestimmten Benutzer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="be559-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="be559-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be559-112">EXAMPLES</span></span>

### <span data-ttu-id="be559-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="be559-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="be559-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be559-114">PARAMETERS</span></span>

### <span data-ttu-id="be559-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be559-115">-DefaultProfile</span></span>
<span data-ttu-id="be559-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be559-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be559-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="be559-117">-DeviceName</span></span>
<span data-ttu-id="be559-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="be559-118">Device Name</span></span>

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

### <span data-ttu-id="be559-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="be559-119">-DeviceObject</span></span>
<span data-ttu-id="be559-120">Geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="be559-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="be559-121">-Name</span><span class="sxs-lookup"><span data-stu-id="be559-121">-Name</span></span>
<span data-ttu-id="be559-122">Benutzername</span><span class="sxs-lookup"><span data-stu-id="be559-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: Username

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be559-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be559-123">-ResourceGroupName</span></span>
<span data-ttu-id="be559-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="be559-124">Resource Group Name</span></span>

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

### <span data-ttu-id="be559-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be559-125">-ResourceId</span></span>
<span data-ttu-id="be559-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="be559-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="be559-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be559-127">CommonParameters</span></span>
<span data-ttu-id="be559-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be559-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be559-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be559-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be559-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be559-130">INPUTS</span></span>

### <span data-ttu-id="be559-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="be559-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="be559-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be559-132">OUTPUTS</span></span>

### <span data-ttu-id="be559-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="be559-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="be559-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="be559-134">NOTES</span></span>

## <span data-ttu-id="be559-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="be559-135">RELATED LINKS</span></span>
