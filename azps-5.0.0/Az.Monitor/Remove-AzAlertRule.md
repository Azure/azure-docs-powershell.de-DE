---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
ms.openlocfilehash: 23b4c81e7c999301ccb535435911a9413ae4ef16
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180117"
---
# <span data-ttu-id="d759f-101">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="d759f-101">Remove-AzAlertRule</span></span>

## <span data-ttu-id="d759f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d759f-102">SYNOPSIS</span></span>
<span data-ttu-id="d759f-103">Entfernt eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="d759f-103">Removes an alert rule.</span></span>

## <span data-ttu-id="d759f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d759f-104">SYNTAX</span></span>

```
Remove-AzAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d759f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d759f-105">DESCRIPTION</span></span>
<span data-ttu-id="d759f-106">Das Cmdlet **Remove-AzAlertRule** entfernt eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="d759f-106">The **Remove-AzAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="d759f-107">Sie müssen den Namen der Warnungsregel und die Ressourcengruppe angeben, der Sie zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d759f-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="d759f-108">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d759f-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="d759f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d759f-109">EXAMPLES</span></span>

### <span data-ttu-id="d759f-110">Beispiel 1: Entfernen einer Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="d759f-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="d759f-111">Dieser Befehl entfernt die Warnungsregel mit dem Namen myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in der Ressourcengruppe Default-Web-centralus.</span><span class="sxs-lookup"><span data-stu-id="d759f-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="d759f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d759f-112">PARAMETERS</span></span>

### <span data-ttu-id="d759f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d759f-113">-DefaultProfile</span></span>
<span data-ttu-id="d759f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d759f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d759f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d759f-115">-Name</span></span>
<span data-ttu-id="d759f-116">Gibt den Namen der zu entfernenden Warnungsregel an.</span><span class="sxs-lookup"><span data-stu-id="d759f-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="d759f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d759f-117">-ResourceGroupName</span></span>
<span data-ttu-id="d759f-118">Gibt den Namen der Ressourcengruppe für die Warnungsregel an.</span><span class="sxs-lookup"><span data-stu-id="d759f-118">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="d759f-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d759f-119">-Confirm</span></span>
<span data-ttu-id="d759f-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d759f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d759f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d759f-121">-WhatIf</span></span>
<span data-ttu-id="d759f-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d759f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d759f-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d759f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d759f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d759f-124">CommonParameters</span></span>
<span data-ttu-id="d759f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d759f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d759f-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d759f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d759f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d759f-127">INPUTS</span></span>

### <span data-ttu-id="d759f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d759f-128">System.String</span></span>

## <span data-ttu-id="d759f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d759f-129">OUTPUTS</span></span>

### <span data-ttu-id="d759f-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d759f-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="d759f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="d759f-131">NOTES</span></span>

## <span data-ttu-id="d759f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d759f-132">RELATED LINKS</span></span>

[<span data-ttu-id="d759f-133">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="d759f-133">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="d759f-134">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="d759f-134">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="d759f-135">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="d759f-135">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="d759f-136">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="d759f-136">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)


