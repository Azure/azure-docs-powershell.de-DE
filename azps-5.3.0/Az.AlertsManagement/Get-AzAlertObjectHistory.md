---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469084"
---
# <span data-ttu-id="70df2-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="70df2-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="70df2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70df2-102">SYNOPSIS</span></span>
<span data-ttu-id="70df2-103">Ruft Benachrichtigungsverlaufsinformationen ab</span><span class="sxs-lookup"><span data-stu-id="70df2-103">Gets Alert History information</span></span>

## <span data-ttu-id="70df2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70df2-104">SYNTAX</span></span>

### <span data-ttu-id="70df2-105">ByAlertId (Standard)</span><span class="sxs-lookup"><span data-stu-id="70df2-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70df2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="70df2-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70df2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70df2-107">DESCRIPTION</span></span>
<span data-ttu-id="70df2-108">**Das Cmdlet "Get-AzAlertObjectHistory"** ruft den Benachrichtigungsverlauf ab.</span><span class="sxs-lookup"><span data-stu-id="70df2-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="70df2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70df2-109">EXAMPLES</span></span>

### <span data-ttu-id="70df2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70df2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="70df2-111">Ruft Benachrichtigungsverlaufsdetails ab.</span><span class="sxs-lookup"><span data-stu-id="70df2-111">Gets alert history details.</span></span> 

## <span data-ttu-id="70df2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70df2-112">PARAMETERS</span></span>

### <span data-ttu-id="70df2-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="70df2-113">-AlertId</span></span>
<span data-ttu-id="70df2-114">Eindeutiger Bezeichner der Warnung/Ressourcen-ID einer Warnung.</span><span class="sxs-lookup"><span data-stu-id="70df2-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70df2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70df2-115">-DefaultProfile</span></span>
<span data-ttu-id="70df2-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70df2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70df2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70df2-117">-InputObject</span></span>
<span data-ttu-id="70df2-118">Eingabeobjekt aus pipeline.</span><span class="sxs-lookup"><span data-stu-id="70df2-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70df2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70df2-119">CommonParameters</span></span>
<span data-ttu-id="70df2-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70df2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70df2-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70df2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70df2-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70df2-122">INPUTS</span></span>

### <span data-ttu-id="70df2-123">Keine</span><span class="sxs-lookup"><span data-stu-id="70df2-123">None</span></span>

## <span data-ttu-id="70df2-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70df2-124">OUTPUTS</span></span>

### <span data-ttu-id="70df2-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="70df2-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="70df2-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="70df2-126">NOTES</span></span>

## <span data-ttu-id="70df2-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="70df2-127">RELATED LINKS</span></span>
