---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 50ffa5beb8ab79d3c903ec5b7e6a21c9b08116db
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406399"
---
# <span data-ttu-id="c792c-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c792c-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="c792c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c792c-102">SYNOPSIS</span></span>
<span data-ttu-id="c792c-103">Ruft mindestens eine Aktivitätsprotokollbenachrichtigungsressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="c792c-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="c792c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c792c-104">SYNTAX</span></span>

### <span data-ttu-id="c792c-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c792c-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c792c-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c792c-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c792c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c792c-107">DESCRIPTION</span></span>
<span data-ttu-id="c792c-108">Das **Cmdlet "Get-AzActivityLogAlert"** ruft eine oder mehrere Ressourcen für Aktivitätsprotokollbenachrichtigungen ab.</span><span class="sxs-lookup"><span data-stu-id="c792c-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="c792c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c792c-109">EXAMPLES</span></span>

### <span data-ttu-id="c792c-110">Beispiel 1: Erhalten von Aktivitätsprotokollbenachrichtigungen nach Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="c792c-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="c792c-111">Dieser Befehl listet alle Aktivitätsprotokollbenachrichtigungen für das aktuelle Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="c792c-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="c792c-112">Beispiel 2: Erhalten von Aktivitätsprotokollbenachrichtigungen für die angegebene Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c792c-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="c792c-113">Dieser Befehl listet Aktivitätsprotokollwarnungen für die angegebene Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="c792c-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="c792c-114">Beispiel 3: Erhalten einer Aktivitätsprotokollbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="c792c-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="c792c-115">Dieser Befehl listet eine Aktivitätsprotokollwarnung (eine Liste mit einem einzelnen Element) auf.</span><span class="sxs-lookup"><span data-stu-id="c792c-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="c792c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c792c-116">PARAMETERS</span></span>

### <span data-ttu-id="c792c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c792c-117">-DefaultProfile</span></span>
<span data-ttu-id="c792c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c792c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c792c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c792c-119">-Name</span></span>
<span data-ttu-id="c792c-120">Der Name der Aktivitätsprotokollbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="c792c-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="c792c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c792c-121">-ResourceGroupName</span></span>
<span data-ttu-id="c792c-122">Der Name der Ressourcengruppe, in der die Warnungsressource vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c792c-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="c792c-123">Wenn "Name" nicht null oder leer ist, muss dieser Parameter eine zeichenfolge enthalten und keine leere Zeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="c792c-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="c792c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c792c-124">CommonParameters</span></span>
<span data-ttu-id="c792c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c792c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c792c-126">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c792c-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c792c-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c792c-127">INPUTS</span></span>

### <span data-ttu-id="c792c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c792c-128">System.String</span></span>

## <span data-ttu-id="c792c-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c792c-129">OUTPUTS</span></span>

### <span data-ttu-id="c792c-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="c792c-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="c792c-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c792c-131">NOTES</span></span>

## <span data-ttu-id="c792c-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c792c-132">RELATED LINKS</span></span>

[<span data-ttu-id="c792c-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c792c-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="c792c-134">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c792c-134">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="c792c-135">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="c792c-135">New-AzActionGroup</span></span>](./New-AzActionGroup.md)
