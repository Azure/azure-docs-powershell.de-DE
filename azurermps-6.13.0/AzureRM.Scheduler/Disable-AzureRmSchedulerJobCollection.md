---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: C06D4AD3-9CB1-4FEB-B02F-74022F264260
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/disable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 9673c236886feb801d6e4078bfccbf82e2339811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482081"
---
# <span data-ttu-id="6821e-101">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6821e-101">Disable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="6821e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6821e-102">SYNOPSIS</span></span>
<span data-ttu-id="6821e-103">Deaktiviert eine Auftrags Sammlung.</span><span class="sxs-lookup"><span data-stu-id="6821e-103">Disables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6821e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6821e-104">SYNTAX</span></span>

```
Disable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6821e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6821e-105">DESCRIPTION</span></span>
<span data-ttu-id="6821e-106">Das Cmdlet **Disable-AzureRmSchedulerJobCollection** deaktiviert eine Auftrags Sammlung in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="6821e-106">The **Disable-AzureRmSchedulerJobCollection** cmdlet disables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="6821e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6821e-107">EXAMPLES</span></span>

## <span data-ttu-id="6821e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6821e-108">PARAMETERS</span></span>

### <span data-ttu-id="6821e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6821e-109">-DefaultProfile</span></span>
<span data-ttu-id="6821e-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6821e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6821e-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="6821e-111">-JobCollectionName</span></span>
<span data-ttu-id="6821e-112">Gibt den Namen einer Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="6821e-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="6821e-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6821e-113">-PassThru</span></span>
<span data-ttu-id="6821e-114">Gibt an, dass dieses Cmdlet den Wert Success für Success zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6821e-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="6821e-115">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="6821e-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6821e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6821e-116">-ResourceGroupName</span></span>
<span data-ttu-id="6821e-117">Gibt die Ressourcengruppe der Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="6821e-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="6821e-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6821e-118">-Confirm</span></span>
<span data-ttu-id="6821e-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6821e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6821e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6821e-120">-WhatIf</span></span>
<span data-ttu-id="6821e-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6821e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6821e-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6821e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6821e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6821e-123">CommonParameters</span></span>
<span data-ttu-id="6821e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6821e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6821e-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6821e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6821e-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6821e-126">INPUTS</span></span>

### <span data-ttu-id="6821e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6821e-127">System.String</span></span>

## <span data-ttu-id="6821e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6821e-128">OUTPUTS</span></span>

### <span data-ttu-id="6821e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6821e-129">System.String</span></span>

## <span data-ttu-id="6821e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="6821e-130">NOTES</span></span>

## <span data-ttu-id="6821e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6821e-131">RELATED LINKS</span></span>

[<span data-ttu-id="6821e-132">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6821e-132">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6821e-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6821e-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6821e-134">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6821e-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6821e-135">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6821e-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6821e-136">Satz-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6821e-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


