---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: da1133895d062e3f49fae0bf6571c3bfeb72992c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664201"
---
# <span data-ttu-id="6e638-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6e638-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="6e638-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e638-102">SYNOPSIS</span></span>
<span data-ttu-id="6e638-103">Ruft Auftrags Auflistungen ab.</span><span class="sxs-lookup"><span data-stu-id="6e638-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e638-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e638-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e638-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e638-105">DESCRIPTION</span></span>
<span data-ttu-id="6e638-106">Das Cmdlet " **Get-AzureRmSchedulerJobCollection** " ruft Auftrags Auflistungen in Azure Scheduler ab.</span><span class="sxs-lookup"><span data-stu-id="6e638-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="6e638-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e638-107">EXAMPLES</span></span>

## <span data-ttu-id="6e638-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e638-108">PARAMETERS</span></span>

### <span data-ttu-id="6e638-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e638-109">-DefaultProfile</span></span>
<span data-ttu-id="6e638-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e638-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e638-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="6e638-111">-JobCollectionName</span></span>
<span data-ttu-id="6e638-112">Gibt den Namen einer Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="6e638-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e638-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e638-113">-ResourceGroupName</span></span>
<span data-ttu-id="6e638-114">Gibt die Ressourcengruppe an, aus der dieses Cmdlet Auftrags Auflistungen erhält.</span><span class="sxs-lookup"><span data-stu-id="6e638-114">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e638-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e638-115">CommonParameters</span></span>
<span data-ttu-id="6e638-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e638-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e638-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e638-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e638-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e638-118">INPUTS</span></span>

### <span data-ttu-id="6e638-119">Keine</span><span class="sxs-lookup"><span data-stu-id="6e638-119">None</span></span>
<span data-ttu-id="6e638-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6e638-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6e638-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e638-121">OUTPUTS</span></span>

### <span data-ttu-id="6e638-122">System. Object</span><span class="sxs-lookup"><span data-stu-id="6e638-122">System.Object</span></span>

## <span data-ttu-id="6e638-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e638-123">NOTES</span></span>

## <span data-ttu-id="6e638-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e638-124">RELATED LINKS</span></span>

[<span data-ttu-id="6e638-125">Deaktivieren-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6e638-125">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6e638-126">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6e638-126">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6e638-127">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6e638-127">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6e638-128">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6e638-128">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6e638-129">Satz-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6e638-129">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


