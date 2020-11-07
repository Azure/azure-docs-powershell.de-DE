---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: af8ef3ef2662dc6793011741fdfd7a903eaa081f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850840"
---
# <span data-ttu-id="6ad85-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6ad85-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="6ad85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ad85-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad85-103">Ruft eine oder mehrere Aktivitätsprotokoll-Warnungs Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="6ad85-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ad85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ad85-104">SYNTAX</span></span>

### <span data-ttu-id="6ad85-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6ad85-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ad85-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6ad85-106">GetByResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ad85-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ad85-107">DESCRIPTION</span></span>
<span data-ttu-id="6ad85-108">Das Cmdlet " **Get-AzureRmActivityLogAlert** " Ruft eine oder mehrere Aktivitätsprotokoll-Warnungs Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="6ad85-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="6ad85-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ad85-109">EXAMPLES</span></span>

### <span data-ttu-id="6ad85-110">Beispiel 1: Abrufen einer Aktivitätsprotokoll Benachrichtigung nach Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="6ad85-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="6ad85-111">Dieser Befehl listet alle Aktivitätsprotokoll Benachrichtigungen für das aktuelle Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="6ad85-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="6ad85-112">Beispiel 2: Abrufen von Benachrichtigungen zum Aktivitätsprotokoll für die angegebene Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6ad85-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="6ad85-113">Dieser Befehl listet Aktivitätsprotokoll Benachrichtigungen für die angegebene Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="6ad85-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="6ad85-114">Beispiel 3: Abrufen einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="6ad85-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="6ad85-115">Dieser Befehl listet eine Benachrichtigung über das Aktivitätsprotokoll (eine Liste mit einem einzelnen Element) auf.</span><span class="sxs-lookup"><span data-stu-id="6ad85-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="6ad85-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ad85-116">PARAMETERS</span></span>

### <span data-ttu-id="6ad85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad85-117">-DefaultProfile</span></span>
<span data-ttu-id="6ad85-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6ad85-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ad85-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6ad85-119">-Name</span></span>
<span data-ttu-id="6ad85-120">Der Name der Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="6ad85-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad85-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad85-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ad85-122">Der Name der Ressourcengruppe, in der die Warnungs Ressource vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6ad85-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="6ad85-123">Wenn Name nicht NULL oder leer ist, muss dieser Parameter eine nicht leere Zeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="6ad85-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad85-124">CommonParameters</span></span>
<span data-ttu-id="6ad85-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad85-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad85-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad85-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ad85-127">INPUTS</span></span>

### <span data-ttu-id="6ad85-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6ad85-128">System.String</span></span>

## <span data-ttu-id="6ad85-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ad85-129">OUTPUTS</span></span>

### <span data-ttu-id="6ad85-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="6ad85-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="6ad85-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ad85-131">NOTES</span></span>

## <span data-ttu-id="6ad85-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ad85-132">RELATED LINKS</span></span>

[<span data-ttu-id="6ad85-133">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6ad85-133">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)



[<span data-ttu-id="6ad85-134">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6ad85-134">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6ad85-135">Neu – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="6ad85-135">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="6ad85-136">Neu – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="6ad85-136">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
