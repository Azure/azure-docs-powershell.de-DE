---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846244"
---
# <span data-ttu-id="02804-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="02804-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="02804-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02804-102">SYNOPSIS</span></span>
<span data-ttu-id="02804-103">Erstellen eines privaten Verknüpfungsbereichs</span><span class="sxs-lookup"><span data-stu-id="02804-103">create private link scope</span></span>

## <span data-ttu-id="02804-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02804-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02804-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02804-105">DESCRIPTION</span></span>
<span data-ttu-id="02804-106">Erstellen eines privaten Verknüpfungsbereichs</span><span class="sxs-lookup"><span data-stu-id="02804-106">create private link scope</span></span>

## <span data-ttu-id="02804-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02804-107">EXAMPLES</span></span>

### <span data-ttu-id="02804-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="02804-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="02804-109">Erstellen eines privaten Verknüpfungsbereichs mit dem Namen "scope_name" unter Ressourcengruppe "rg_name" an Position "eastus"</span><span class="sxs-lookup"><span data-stu-id="02804-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="02804-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="02804-110">PARAMETERS</span></span>

### <span data-ttu-id="02804-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02804-111">-DefaultProfile</span></span>
<span data-ttu-id="02804-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02804-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02804-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="02804-113">-Location</span></span>
<span data-ttu-id="02804-114">Lage</span><span class="sxs-lookup"><span data-stu-id="02804-114">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02804-115">-Name</span><span class="sxs-lookup"><span data-stu-id="02804-115">-Name</span></span>
<span data-ttu-id="02804-116">Name des privaten Link Bereichs</span><span class="sxs-lookup"><span data-stu-id="02804-116">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02804-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02804-117">-ResourceGroupName</span></span>
<span data-ttu-id="02804-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="02804-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02804-119">-Tags</span><span class="sxs-lookup"><span data-stu-id="02804-119">-Tags</span></span>
<span data-ttu-id="02804-120">Tags</span><span class="sxs-lookup"><span data-stu-id="02804-120">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02804-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="02804-121">-Confirm</span></span>
<span data-ttu-id="02804-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02804-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02804-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02804-123">-WhatIf</span></span>
<span data-ttu-id="02804-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02804-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02804-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02804-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02804-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02804-126">CommonParameters</span></span>
<span data-ttu-id="02804-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02804-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02804-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02804-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02804-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02804-129">INPUTS</span></span>

### <span data-ttu-id="02804-130">System. String</span><span class="sxs-lookup"><span data-stu-id="02804-130">System.String</span></span>

## <span data-ttu-id="02804-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02804-131">OUTPUTS</span></span>

### <span data-ttu-id="02804-132">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="02804-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="02804-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="02804-133">NOTES</span></span>

## <span data-ttu-id="02804-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02804-134">RELATED LINKS</span></span>
