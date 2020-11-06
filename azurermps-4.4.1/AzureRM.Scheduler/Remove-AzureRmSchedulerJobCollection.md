---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F315B193-C17B-41A9-B61D-0A0212B6B643
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: b1caa041f92312d3d122e758a9e63bc7299887b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496902"
---
# <span data-ttu-id="d2ed6-101">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d2ed6-101">Remove-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="d2ed6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ed6-103">Entfernt eine Auftrags Sammlung.</span><span class="sxs-lookup"><span data-stu-id="d2ed6-103">Removes a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2ed6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2ed6-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2ed6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2ed6-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ed6-106">Das Cmdlet " **Remove-AzureRmSchedulerJobCollection** " entfernt eine Auftrags Sammlung im Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="d2ed6-106">The **Remove-AzureRmSchedulerJobCollection** cmdlet removes a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="d2ed6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2ed6-107">EXAMPLES</span></span>

## <span data-ttu-id="d2ed6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2ed6-108">PARAMETERS</span></span>

### <span data-ttu-id="d2ed6-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d2ed6-109">-JobCollectionName</span></span>
<span data-ttu-id="d2ed6-110">Gibt den Namen einer Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="d2ed6-110">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed6-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2ed6-111">-PassThru</span></span>
<span data-ttu-id="d2ed6-112">Gibt an, dass dieses Cmdlet den Wert Success für Success zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d2ed6-112">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="d2ed6-113">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d2ed6-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d2ed6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ed6-114">-ResourceGroupName</span></span>
<span data-ttu-id="d2ed6-115">Gibt die Ressourcengruppe der Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="d2ed6-115">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="d2ed6-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d2ed6-116">-Confirm</span></span>
<span data-ttu-id="d2ed6-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2ed6-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ed6-118">-WhatIf</span></span>
<span data-ttu-id="d2ed6-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2ed6-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2ed6-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2ed6-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ed6-121">-DefaultProfile</span></span>
<span data-ttu-id="d2ed6-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2ed6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2ed6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ed6-123">CommonParameters</span></span>
<span data-ttu-id="d2ed6-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ed6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ed6-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ed6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ed6-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2ed6-126">INPUTS</span></span>

## <span data-ttu-id="d2ed6-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2ed6-127">OUTPUTS</span></span>

## <span data-ttu-id="d2ed6-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2ed6-128">NOTES</span></span>

## <span data-ttu-id="d2ed6-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2ed6-129">RELATED LINKS</span></span>

[<span data-ttu-id="d2ed6-130">Deaktivieren-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d2ed6-130">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d2ed6-131">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d2ed6-131">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d2ed6-132">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d2ed6-132">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d2ed6-133">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d2ed6-133">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d2ed6-134">Satz-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d2ed6-134">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


