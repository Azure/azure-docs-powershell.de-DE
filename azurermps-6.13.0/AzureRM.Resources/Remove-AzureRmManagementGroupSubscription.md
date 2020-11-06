---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroupSubscription.md
ms.openlocfilehash: 882583c50db8a4b4473bce829aab120a68478434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477717"
---
# <span data-ttu-id="f1966-101">Remove-AzureRmManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="f1966-101">Remove-AzureRmManagementGroupSubscription</span></span>

## <span data-ttu-id="f1966-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1966-102">SYNOPSIS</span></span>
<span data-ttu-id="f1966-103">Entfernt ein Abonnement aus einer Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f1966-103">Removes a Subscription from a Management Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1966-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1966-104">SYNTAX</span></span>

```
Remove-AzureRmManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1966-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1966-105">DESCRIPTION</span></span>
<span data-ttu-id="f1966-106">Das Cmdlet **Remove-AzureRmManagementGroupSubscription** entfernt ein Abonnement aus einer Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f1966-106">The **Remove-AzureRmManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="f1966-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1966-107">EXAMPLES</span></span>

### <span data-ttu-id="f1966-108">Beispiel 1 – Entfernen des Abonnements aus einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="f1966-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="f1966-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1966-109">PARAMETERS</span></span>

### <span data-ttu-id="f1966-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1966-110">-DefaultProfile</span></span>
<span data-ttu-id="f1966-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1966-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1966-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="f1966-112">-GroupName</span></span>
<span data-ttu-id="f1966-113">Verwaltungsgruppen-ID</span><span class="sxs-lookup"><span data-stu-id="f1966-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1966-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1966-114">-PassThru</span></span>
<span data-ttu-id="f1966-115">Zurück `true` zur erfolgreichen Ausführung</span><span class="sxs-lookup"><span data-stu-id="f1966-115">Return `true` on successful execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1966-116">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f1966-116">-SubscriptionId</span></span>
<span data-ttu-id="f1966-117">Abonnement-ID des Abonnements, das der Verwaltung zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="f1966-117">Subscription Id of the subscription associated witht the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1966-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1966-118">-Confirm</span></span>
<span data-ttu-id="f1966-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1966-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1966-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1966-120">-WhatIf</span></span>
<span data-ttu-id="f1966-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1966-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1966-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1966-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1966-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1966-123">CommonParameters</span></span>
<span data-ttu-id="f1966-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1966-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1966-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1966-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1966-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1966-126">INPUTS</span></span>

### <span data-ttu-id="f1966-127">Keine</span><span class="sxs-lookup"><span data-stu-id="f1966-127">None</span></span>

## <span data-ttu-id="f1966-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1966-128">OUTPUTS</span></span>

### <span data-ttu-id="f1966-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1966-129">System.Boolean</span></span>

## <span data-ttu-id="f1966-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1966-130">NOTES</span></span>

## <span data-ttu-id="f1966-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1966-131">RELATED LINKS</span></span>
