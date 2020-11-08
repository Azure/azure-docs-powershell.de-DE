---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176835"
---
# <span data-ttu-id="c20f7-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="c20f7-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="c20f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c20f7-102">SYNOPSIS</span></span>
<span data-ttu-id="c20f7-103">Ruft die konfigurierten Benutzer für ein Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="c20f7-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="c20f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c20f7-104">SYNTAX</span></span>

### <span data-ttu-id="c20f7-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c20f7-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c20f7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c20f7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c20f7-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c20f7-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c20f7-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c20f7-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="c20f7-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c20f7-109">DESCRIPTION</span></span>
<span data-ttu-id="c20f7-110">Das Cmdlet " **Get-AzStackEdgeUser** " listet die Benutzer auf, die für ein Stack-Edge-Gerät konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="c20f7-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="c20f7-111">Sie können den Namen in Parametern erwähnen, um Details zu einem bestimmten Benutzer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c20f7-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="c20f7-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c20f7-112">EXAMPLES</span></span>

### <span data-ttu-id="c20f7-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c20f7-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="c20f7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c20f7-114">PARAMETERS</span></span>

### <span data-ttu-id="c20f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c20f7-115">-DefaultProfile</span></span>
<span data-ttu-id="c20f7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c20f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c20f7-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c20f7-117">-DeviceName</span></span>
<span data-ttu-id="c20f7-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="c20f7-118">Device Name</span></span>

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

### <span data-ttu-id="c20f7-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c20f7-119">-DeviceObject</span></span>
<span data-ttu-id="c20f7-120">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="c20f7-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="c20f7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c20f7-121">-Name</span></span>
<span data-ttu-id="c20f7-122">Username</span><span class="sxs-lookup"><span data-stu-id="c20f7-122">Username</span></span>

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

### <span data-ttu-id="c20f7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c20f7-123">-ResourceGroupName</span></span>
<span data-ttu-id="c20f7-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="c20f7-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c20f7-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c20f7-125">-ResourceId</span></span>
<span data-ttu-id="c20f7-126">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="c20f7-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="c20f7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c20f7-127">CommonParameters</span></span>
<span data-ttu-id="c20f7-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c20f7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c20f7-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c20f7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c20f7-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c20f7-130">INPUTS</span></span>

### <span data-ttu-id="c20f7-131">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c20f7-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="c20f7-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c20f7-132">OUTPUTS</span></span>

### <span data-ttu-id="c20f7-133">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="c20f7-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="c20f7-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="c20f7-134">NOTES</span></span>

## <span data-ttu-id="c20f7-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c20f7-135">RELATED LINKS</span></span>
