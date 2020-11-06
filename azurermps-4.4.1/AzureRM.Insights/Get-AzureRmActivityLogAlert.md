---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: b4a1204d25852aa75c7b68c90305aefe9cfefe6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504942"
---
# <span data-ttu-id="fb7a0-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fb7a0-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="fb7a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb7a0-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7a0-103">Ruft eine oder mehrere Aktivitätsprotokoll-Warnungs Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="fb7a0-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb7a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb7a0-104">SYNTAX</span></span>

### <span data-ttu-id="fb7a0-105">Standardparameter für die Benachrichtigung "Aktivitätsprotokoll abrufen"</span><span class="sxs-lookup"><span data-stu-id="fb7a0-105">Default parameters for get an activity log alert</span></span>
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb7a0-106">Parameter, um sicherzustellen, dass die Ressourcengruppe angegeben wird, wenn der Name angegeben wird</span><span class="sxs-lookup"><span data-stu-id="fb7a0-106">Parameters to make sure the resource group is given when the name is given</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb7a0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb7a0-107">DESCRIPTION</span></span>
<span data-ttu-id="fb7a0-108">Das Cmdlet " **Get-AzureRmActivityLogAlert** " Ruft eine oder mehrere Aktivitätsprotokoll-Warnungs Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="fb7a0-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="fb7a0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb7a0-109">EXAMPLES</span></span>

### <span data-ttu-id="fb7a0-110">Beispiel 1: Abrufen einer Aktivitätsprotokoll Benachrichtigung nach Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="fb7a0-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="fb7a0-111">Dieser Befehl listet alle Aktivitätsprotokoll Benachrichtigungen für das aktuelle Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="fb7a0-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="fb7a0-112">Beispiel 2: Abrufen von Benachrichtigungen zum Aktivitätsprotokoll für die angegebene Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fb7a0-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="fb7a0-113">Dieser Befehl listet Aktivitätsprotokoll Benachrichtigungen für die angegebene Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="fb7a0-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="fb7a0-114">Beispiel 3: Abrufen einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="fb7a0-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="fb7a0-115">Dieser Befehl listet eine Benachrichtigung über das Aktivitätsprotokoll (eine Liste mit einem einzelnen Element) auf.</span><span class="sxs-lookup"><span data-stu-id="fb7a0-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="fb7a0-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb7a0-116">PARAMETERS</span></span>

### <span data-ttu-id="fb7a0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fb7a0-117">-Name</span></span>
<span data-ttu-id="fb7a0-118">Der Name der Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="fb7a0-118">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7a0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb7a0-119">-ResourceGroupName</span></span>
<span data-ttu-id="fb7a0-120">Der Name der Ressourcengruppe, in der die Warnungs Ressource vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fb7a0-120">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="fb7a0-121">Wenn Name nicht NULL oder leer ist, muss dieser Parameter eine nicht leere Zeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="fb7a0-121">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to make sure the resource group is given when the name is given
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7a0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7a0-122">-DefaultProfile</span></span>
<span data-ttu-id="fb7a0-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb7a0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb7a0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7a0-124">CommonParameters</span></span>
<span data-ttu-id="fb7a0-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7a0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7a0-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb7a0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7a0-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb7a0-127">INPUTS</span></span>

### <span data-ttu-id="fb7a0-128">Keine</span><span class="sxs-lookup"><span data-stu-id="fb7a0-128">None</span></span>

## <span data-ttu-id="fb7a0-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb7a0-129">OUTPUTS</span></span>

### <span data-ttu-id="fb7a0-130"><System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource]</span><span class="sxs-lookup"><span data-stu-id="fb7a0-130"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource]</span></span>

### <span data-ttu-id="fb7a0-131">Keine</span><span class="sxs-lookup"><span data-stu-id="fb7a0-131">None</span></span>

## <span data-ttu-id="fb7a0-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb7a0-132">NOTES</span></span>

## <span data-ttu-id="fb7a0-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb7a0-133">RELATED LINKS</span></span>

[<span data-ttu-id="fb7a0-134">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fb7a0-134">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="fb7a0-135">Update-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fb7a0-135">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="fb7a0-136">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fb7a0-136">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="fb7a0-137">Neu – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="fb7a0-137">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="fb7a0-138">Neu – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="fb7a0-138">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
