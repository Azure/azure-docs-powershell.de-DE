---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
ms.openlocfilehash: 21cc1e70e0122e21dac5cb78cfa4f4346cf72e5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822651"
---
# <span data-ttu-id="5d033-101">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5d033-101">Remove-AzAutoscaleSetting</span></span>

## <span data-ttu-id="5d033-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d033-102">SYNOPSIS</span></span>
<span data-ttu-id="5d033-103">Entfernt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="5d033-103">Removes an Autoscale setting.</span></span>

## <span data-ttu-id="5d033-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d033-104">SYNTAX</span></span>

```
Remove-AzAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d033-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d033-105">DESCRIPTION</span></span>
<span data-ttu-id="5d033-106">Das Cmdlet **Remove-AzAutoscaleSetting** entfernt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="5d033-106">The **Remove-AzAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="5d033-107">Sie müssen den Namen der Einstellung und den Namen der Ressourcengruppe angeben, der Sie zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="5d033-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="5d033-108">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5d033-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="5d033-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d033-109">EXAMPLES</span></span>

## <span data-ttu-id="5d033-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d033-110">PARAMETERS</span></span>

### <span data-ttu-id="5d033-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d033-111">-DefaultProfile</span></span>
<span data-ttu-id="5d033-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5d033-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d033-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5d033-113">-Name</span></span>
<span data-ttu-id="5d033-114">Gibt den Namen der zu entfernenden AutoScale-Einstellung an.</span><span class="sxs-lookup"><span data-stu-id="5d033-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="5d033-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d033-115">-ResourceGroupName</span></span>
<span data-ttu-id="5d033-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5d033-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5d033-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d033-117">-Confirm</span></span>
<span data-ttu-id="5d033-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d033-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d033-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d033-119">-WhatIf</span></span>
<span data-ttu-id="5d033-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d033-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d033-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d033-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d033-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d033-122">CommonParameters</span></span>
<span data-ttu-id="5d033-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d033-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d033-124">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d033-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d033-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d033-125">INPUTS</span></span>

### <span data-ttu-id="5d033-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5d033-126">System.String</span></span>

## <span data-ttu-id="5d033-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d033-127">OUTPUTS</span></span>

### <span data-ttu-id="5d033-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5d033-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="5d033-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d033-129">NOTES</span></span>

## <span data-ttu-id="5d033-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d033-130">RELATED LINKS</span></span>

[<span data-ttu-id="5d033-131">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5d033-131">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="5d033-132">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5d033-132">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)


