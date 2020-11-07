---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 7a881b6479561ac7a616158c8054bff592209289
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850848"
---
# <span data-ttu-id="4cf08-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="4cf08-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="4cf08-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4cf08-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf08-103">Ruft die Aktionsgruppe (n) ab.</span><span class="sxs-lookup"><span data-stu-id="4cf08-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cf08-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cf08-104">SYNTAX</span></span>

### <span data-ttu-id="4cf08-105">BySubscriptionOrResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="4cf08-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cf08-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4cf08-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cf08-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cf08-107">DESCRIPTION</span></span>
<span data-ttu-id="4cf08-108">Das Cmdlet " **Get-AzureRmActionGroup** " ruft mindestens eine Aktionsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="4cf08-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="4cf08-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4cf08-109">EXAMPLES</span></span>

### <span data-ttu-id="4cf08-110">Beispiel 1: Abrufen einer Aktionsgruppe nach Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="4cf08-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="4cf08-111">Dieser Befehl listet alle Aktionsgruppen für das aktuelle Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="4cf08-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="4cf08-112">Beispiel 2: Abrufen von Aktionsgruppen für die angegebene Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4cf08-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="4cf08-113">Dieser Befehl listet Aktionsgruppen für die angegebene Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="4cf08-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="4cf08-114">Beispiel 3: Abrufen einer Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="4cf08-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="4cf08-115">Dieser Befehl listet eine Aktionsgruppe (eine Liste mit einem einzelnen Element) auf.</span><span class="sxs-lookup"><span data-stu-id="4cf08-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="4cf08-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cf08-116">PARAMETERS</span></span>

### <span data-ttu-id="4cf08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf08-117">-DefaultProfile</span></span>
<span data-ttu-id="4cf08-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4cf08-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf08-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4cf08-119">-Name</span></span>
<span data-ttu-id="4cf08-120">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="4cf08-120">The name of the action group.</span></span>

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

### <span data-ttu-id="4cf08-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf08-121">-ResourceGroupName</span></span>
<span data-ttu-id="4cf08-122">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4cf08-122">The resource group name</span></span>

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

### <span data-ttu-id="4cf08-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf08-123">CommonParameters</span></span>
<span data-ttu-id="4cf08-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf08-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf08-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cf08-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf08-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4cf08-126">INPUTS</span></span>

### <span data-ttu-id="4cf08-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4cf08-127">System.String</span></span>

## <span data-ttu-id="4cf08-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4cf08-128">OUTPUTS</span></span>

### <span data-ttu-id="4cf08-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="4cf08-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="4cf08-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="4cf08-130">NOTES</span></span>

## <span data-ttu-id="4cf08-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4cf08-131">RELATED LINKS</span></span>

<span data-ttu-id="4cf08-132">[Satz-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Neu – AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="4cf08-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
