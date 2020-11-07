---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: 92550ee9f5eed7cf31624748140a0355ac6849ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664608"
---
# <span data-ttu-id="21b84-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="21b84-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="21b84-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21b84-102">SYNOPSIS</span></span>
<span data-ttu-id="21b84-103">Ruft eine oder mehrere Aktivitätsprotokoll-Warnungs Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="21b84-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21b84-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21b84-104">SYNTAX</span></span>

### <span data-ttu-id="21b84-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="21b84-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21b84-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="21b84-106">GetByResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21b84-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21b84-107">DESCRIPTION</span></span>
<span data-ttu-id="21b84-108">Das Cmdlet " **Get-AzureRmActivityLogAlert** " Ruft eine oder mehrere Aktivitätsprotokoll-Warnungs Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="21b84-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="21b84-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21b84-109">EXAMPLES</span></span>

### <span data-ttu-id="21b84-110">Beispiel 1: Abrufen einer Aktivitätsprotokoll Benachrichtigung nach Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="21b84-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="21b84-111">Dieser Befehl listet alle Aktivitätsprotokoll Benachrichtigungen für das aktuelle Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="21b84-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="21b84-112">Beispiel 2: Abrufen von Benachrichtigungen zum Aktivitätsprotokoll für die angegebene Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="21b84-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="21b84-113">Dieser Befehl listet Aktivitätsprotokoll Benachrichtigungen für die angegebene Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="21b84-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="21b84-114">Beispiel 3: Abrufen einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="21b84-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="21b84-115">Dieser Befehl listet eine Benachrichtigung über das Aktivitätsprotokoll (eine Liste mit einem einzelnen Element) auf.</span><span class="sxs-lookup"><span data-stu-id="21b84-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="21b84-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="21b84-116">PARAMETERS</span></span>

### <span data-ttu-id="21b84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21b84-117">-DefaultProfile</span></span>
<span data-ttu-id="21b84-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="21b84-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21b84-119">-Name</span><span class="sxs-lookup"><span data-stu-id="21b84-119">-Name</span></span>
<span data-ttu-id="21b84-120">Der Name der Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="21b84-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="21b84-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21b84-121">-ResourceGroupName</span></span>
<span data-ttu-id="21b84-122">Der Name der Ressourcengruppe, in der die Warnungs Ressource vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="21b84-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="21b84-123">Wenn Name nicht NULL oder leer ist, muss dieser Parameter eine nicht leere Zeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="21b84-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="21b84-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21b84-124">CommonParameters</span></span>
<span data-ttu-id="21b84-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21b84-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21b84-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21b84-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21b84-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21b84-127">INPUTS</span></span>

### <span data-ttu-id="21b84-128">System. String</span><span class="sxs-lookup"><span data-stu-id="21b84-128">System.String</span></span>

## <span data-ttu-id="21b84-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21b84-129">OUTPUTS</span></span>

### <span data-ttu-id="21b84-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="21b84-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="21b84-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="21b84-131">NOTES</span></span>

## <span data-ttu-id="21b84-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21b84-132">RELATED LINKS</span></span>

[<span data-ttu-id="21b84-133">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="21b84-133">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="21b84-134">Update-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="21b84-134">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="21b84-135">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="21b84-135">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="21b84-136">Neu – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="21b84-136">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="21b84-137">Neu – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="21b84-137">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
