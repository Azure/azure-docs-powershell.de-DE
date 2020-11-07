---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
ms.openlocfilehash: b0fc044ee2a4704c9bb6803ab0cf7a4be4ea95e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849319"
---
# <span data-ttu-id="78e0a-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="78e0a-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="78e0a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="78e0a-103">Entfernt eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="78e0a-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78e0a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78e0a-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78e0a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78e0a-105">DESCRIPTION</span></span>
<span data-ttu-id="78e0a-106">Das Cmdlet **Remove-AzureRmAlertRule** entfernt eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="78e0a-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="78e0a-107">Sie müssen den Namen der Warnungsregel und die Ressourcengruppe angeben, der Sie zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="78e0a-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="78e0a-108">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="78e0a-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="78e0a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78e0a-109">EXAMPLES</span></span>

### <span data-ttu-id="78e0a-110">Beispiel 1: Entfernen einer Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="78e0a-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="78e0a-111">Dieser Befehl entfernt die Warnungsregel mit dem Namen myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in der Ressourcengruppe Default-Web-centralus.</span><span class="sxs-lookup"><span data-stu-id="78e0a-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="78e0a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="78e0a-112">PARAMETERS</span></span>

### <span data-ttu-id="78e0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e0a-113">-DefaultProfile</span></span>
<span data-ttu-id="78e0a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="78e0a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78e0a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="78e0a-115">-Name</span></span>
<span data-ttu-id="78e0a-116">Gibt den Namen der zu entfernenden Warnungsregel an.</span><span class="sxs-lookup"><span data-stu-id="78e0a-116">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e0a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78e0a-117">-ResourceGroupName</span></span>
<span data-ttu-id="78e0a-118">Gibt den Namen der Ressourcengruppe für die Warnungsregel an.</span><span class="sxs-lookup"><span data-stu-id="78e0a-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e0a-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78e0a-119">-Confirm</span></span>
<span data-ttu-id="78e0a-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78e0a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e0a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78e0a-121">-WhatIf</span></span>
<span data-ttu-id="78e0a-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78e0a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78e0a-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78e0a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e0a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e0a-124">CommonParameters</span></span>
<span data-ttu-id="78e0a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78e0a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e0a-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78e0a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e0a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78e0a-127">INPUTS</span></span>

### <span data-ttu-id="78e0a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="78e0a-128">System.String</span></span>

## <span data-ttu-id="78e0a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78e0a-129">OUTPUTS</span></span>

### <span data-ttu-id="78e0a-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="78e0a-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="78e0a-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="78e0a-131">NOTES</span></span>

## <span data-ttu-id="78e0a-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78e0a-132">RELATED LINKS</span></span>

[<span data-ttu-id="78e0a-133">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="78e0a-133">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="78e0a-134">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="78e0a-134">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="78e0a-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="78e0a-135">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="78e0a-136">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="78e0a-136">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


