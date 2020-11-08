---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 030564f700f399b1880d36e4dac628a9fc3efa35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178815"
---
# <span data-ttu-id="619f1-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="619f1-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="619f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="619f1-102">SYNOPSIS</span></span>
<span data-ttu-id="619f1-103">Ruft eine oder mehrere Aktivitätsprotokoll-Warnungs Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="619f1-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="619f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="619f1-104">SYNTAX</span></span>

### <span data-ttu-id="619f1-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="619f1-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="619f1-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="619f1-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="619f1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="619f1-107">DESCRIPTION</span></span>
<span data-ttu-id="619f1-108">Das Cmdlet " **Get-AzActivityLogAlert** " Ruft eine oder mehrere Aktivitätsprotokoll-Warnungs Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="619f1-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="619f1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="619f1-109">EXAMPLES</span></span>

### <span data-ttu-id="619f1-110">Beispiel 1: Abrufen einer Aktivitätsprotokoll Benachrichtigung nach Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="619f1-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="619f1-111">Dieser Befehl listet alle Aktivitätsprotokoll Benachrichtigungen für das aktuelle Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="619f1-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="619f1-112">Beispiel 2: Abrufen von Benachrichtigungen zum Aktivitätsprotokoll für die angegebene Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="619f1-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="619f1-113">Dieser Befehl listet Aktivitätsprotokoll Benachrichtigungen für die angegebene Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="619f1-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="619f1-114">Beispiel 3: Abrufen einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="619f1-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="619f1-115">Dieser Befehl listet eine Benachrichtigung über das Aktivitätsprotokoll (eine Liste mit einem einzelnen Element) auf.</span><span class="sxs-lookup"><span data-stu-id="619f1-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="619f1-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="619f1-116">PARAMETERS</span></span>

### <span data-ttu-id="619f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="619f1-117">-DefaultProfile</span></span>
<span data-ttu-id="619f1-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="619f1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="619f1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="619f1-119">-Name</span></span>
<span data-ttu-id="619f1-120">Der Name der Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="619f1-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="619f1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="619f1-121">-ResourceGroupName</span></span>
<span data-ttu-id="619f1-122">Der Name der Ressourcengruppe, in der die Warnungs Ressource vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="619f1-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="619f1-123">Wenn Name nicht NULL oder leer ist, muss dieser Parameter eine nicht leere Zeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="619f1-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="619f1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="619f1-124">CommonParameters</span></span>
<span data-ttu-id="619f1-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="619f1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="619f1-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="619f1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="619f1-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="619f1-127">INPUTS</span></span>

### <span data-ttu-id="619f1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="619f1-128">System.String</span></span>

## <span data-ttu-id="619f1-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="619f1-129">OUTPUTS</span></span>

### <span data-ttu-id="619f1-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="619f1-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="619f1-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="619f1-131">NOTES</span></span>

## <span data-ttu-id="619f1-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="619f1-132">RELATED LINKS</span></span>

[<span data-ttu-id="619f1-133">Satz-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="619f1-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="619f1-134">Update-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="619f1-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="619f1-135">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="619f1-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="619f1-136">Neu – AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="619f1-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="619f1-137">Neu – AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="619f1-137">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
