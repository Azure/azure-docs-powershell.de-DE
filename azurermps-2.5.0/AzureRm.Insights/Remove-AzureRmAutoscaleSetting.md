---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 93c51e71cf912a072daafd721d9e9626ccefbb06
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849296"
---
# <span data-ttu-id="c9bb0-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c9bb0-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="c9bb0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="c9bb0-103">Entfernt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="c9bb0-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9bb0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9bb0-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9bb0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9bb0-105">DESCRIPTION</span></span>
<span data-ttu-id="c9bb0-106">Das Cmdlet **Remove-AzureRmAutoscaleSetting** entfernt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="c9bb0-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="c9bb0-107">Sie müssen den Namen der Einstellung und den Namen der Ressourcengruppe angeben, der Sie zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c9bb0-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="c9bb0-108">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c9bb0-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c9bb0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9bb0-109">EXAMPLES</span></span>

## <span data-ttu-id="c9bb0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9bb0-110">PARAMETERS</span></span>

### <span data-ttu-id="c9bb0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9bb0-111">-DefaultProfile</span></span>
<span data-ttu-id="c9bb0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c9bb0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9bb0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c9bb0-113">-Name</span></span>
<span data-ttu-id="c9bb0-114">Gibt den Namen der zu entfernenden AutoScale-Einstellung an.</span><span class="sxs-lookup"><span data-stu-id="c9bb0-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="c9bb0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9bb0-115">-ResourceGroupName</span></span>
<span data-ttu-id="c9bb0-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c9bb0-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c9bb0-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c9bb0-117">-Confirm</span></span>
<span data-ttu-id="c9bb0-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9bb0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9bb0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9bb0-119">-WhatIf</span></span>
<span data-ttu-id="c9bb0-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9bb0-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9bb0-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9bb0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9bb0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9bb0-122">CommonParameters</span></span>
<span data-ttu-id="c9bb0-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9bb0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9bb0-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9bb0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9bb0-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9bb0-125">INPUTS</span></span>

### <span data-ttu-id="c9bb0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c9bb0-126">System.String</span></span>

## <span data-ttu-id="c9bb0-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9bb0-127">OUTPUTS</span></span>

### <span data-ttu-id="c9bb0-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c9bb0-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="c9bb0-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9bb0-129">NOTES</span></span>

## <span data-ttu-id="c9bb0-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9bb0-130">RELATED LINKS</span></span>

[<span data-ttu-id="c9bb0-131">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c9bb0-131">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="c9bb0-132">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c9bb0-132">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


