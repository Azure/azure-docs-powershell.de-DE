---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: cb1da61809b293c66dfb9fc0b5e067e03d34aefe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932723"
---
# <span data-ttu-id="1a033-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="1a033-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="1a033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a033-102">SYNOPSIS</span></span>
<span data-ttu-id="1a033-103">Ruft Aktionsgruppe(en) ab.</span><span class="sxs-lookup"><span data-stu-id="1a033-103">Gets action group(s).</span></span>

## <span data-ttu-id="1a033-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a033-104">SYNTAX</span></span>

### <span data-ttu-id="1a033-105">BySubscriptionOrResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="1a033-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a033-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1a033-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a033-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a033-107">DESCRIPTION</span></span>
<span data-ttu-id="1a033-108">Das **Cmdlet Get-AzActionGroup** ruft eine oder mehrere Aktionsgruppen ab.</span><span class="sxs-lookup"><span data-stu-id="1a033-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="1a033-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a033-109">EXAMPLES</span></span>

### <span data-ttu-id="1a033-110">Beispiel 1: Erhalten einer Aktionsgruppe nach Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="1a033-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="1a033-111">Mit diesem Befehl werden alle Aktionsgruppen für das aktuelle Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a033-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="1a033-112">Beispiel 2: Erhalten von Aktionsgruppen für die angegebene Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1a033-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="1a033-113">Mit diesem Befehl werden Aktionsgruppen für die angegebene Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a033-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="1a033-114">Beispiel 3: Eine Aktionsgruppe erhalten.</span><span class="sxs-lookup"><span data-stu-id="1a033-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="1a033-115">Mit diesem Befehl wird eine Aktionsgruppe (eine Liste mit einem einzelnen Element) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a033-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="1a033-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1a033-116">PARAMETERS</span></span>

### <span data-ttu-id="1a033-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a033-117">-DefaultProfile</span></span>
<span data-ttu-id="1a033-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1a033-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a033-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1a033-119">-Name</span></span>
<span data-ttu-id="1a033-120">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="1a033-120">The name of the action group.</span></span>

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

### <span data-ttu-id="1a033-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a033-121">-ResourceGroupName</span></span>
<span data-ttu-id="1a033-122">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1a033-122">The resource group name</span></span>

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

### <span data-ttu-id="1a033-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a033-123">CommonParameters</span></span>
<span data-ttu-id="1a033-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a033-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a033-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a033-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a033-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a033-126">INPUTS</span></span>

### <span data-ttu-id="1a033-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1a033-127">System.String</span></span>

## <span data-ttu-id="1a033-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a033-128">OUTPUTS</span></span>

### <span data-ttu-id="1a033-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="1a033-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="1a033-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1a033-130">NOTES</span></span>

## <span data-ttu-id="1a033-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1a033-131">RELATED LINKS</span></span>

<span data-ttu-id="1a033-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="1a033-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
