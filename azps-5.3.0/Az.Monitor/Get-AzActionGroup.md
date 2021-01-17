---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: 90bd9c7943e6e788d81f8ddec85513676afade23
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470409"
---
# <span data-ttu-id="0b8cd-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="0b8cd-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="0b8cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b8cd-102">SYNOPSIS</span></span>
<span data-ttu-id="0b8cd-103">Ruft Aktionsgruppe(n) ab.</span><span class="sxs-lookup"><span data-stu-id="0b8cd-103">Gets action group(s).</span></span>

## <span data-ttu-id="0b8cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b8cd-104">SYNTAX</span></span>

### <span data-ttu-id="0b8cd-105">BySubscriptionOrResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b8cd-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b8cd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0b8cd-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b8cd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b8cd-107">DESCRIPTION</span></span>
<span data-ttu-id="0b8cd-108">Das **Get-AzActionGroup-Cmdlet** ruft mindestens eine Aktionsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0b8cd-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="0b8cd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b8cd-109">EXAMPLES</span></span>

### <span data-ttu-id="0b8cd-110">Beispiel 1: Erhalten einer Aktionsgruppe nach Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="0b8cd-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="0b8cd-111">Mit diesem Befehl werden alle Aktionsgruppe für das aktuelle Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b8cd-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="0b8cd-112">Beispiel 2: Erhalten von Aktionsgruppen für die angegebene Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0b8cd-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="0b8cd-113">Dieser Befehl listet Aktionsgruppen für die angegebene Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="0b8cd-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="0b8cd-114">Beispiel 3: Erhalten einer Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="0b8cd-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="0b8cd-115">Dieser Befehl listet eine Aktionsgruppe (eine Liste mit einem einzelnen Element) auf.</span><span class="sxs-lookup"><span data-stu-id="0b8cd-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="0b8cd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b8cd-116">PARAMETERS</span></span>

### <span data-ttu-id="0b8cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b8cd-117">-DefaultProfile</span></span>
<span data-ttu-id="0b8cd-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0b8cd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b8cd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0b8cd-119">-Name</span></span>
<span data-ttu-id="0b8cd-120">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0b8cd-120">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b8cd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b8cd-121">-ResourceGroupName</span></span>
<span data-ttu-id="0b8cd-122">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0b8cd-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b8cd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b8cd-123">CommonParameters</span></span>
<span data-ttu-id="0b8cd-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b8cd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b8cd-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b8cd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b8cd-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b8cd-126">INPUTS</span></span>

### <span data-ttu-id="0b8cd-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0b8cd-127">System.String</span></span>

## <span data-ttu-id="0b8cd-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b8cd-128">OUTPUTS</span></span>

### <span data-ttu-id="0b8cd-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="0b8cd-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="0b8cd-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0b8cd-130">NOTES</span></span>

## <span data-ttu-id="0b8cd-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0b8cd-131">RELATED LINKS</span></span>

<span data-ttu-id="0b8cd-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="0b8cd-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
