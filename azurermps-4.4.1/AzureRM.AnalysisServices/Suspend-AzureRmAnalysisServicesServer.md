---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 35b8788c67098a45f6a5373e90b7a93fbcbc4703
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477469"
---
# <span data-ttu-id="eea25-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="eea25-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="eea25-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eea25-102">SYNOPSIS</span></span>
<span data-ttu-id="eea25-103">Unterbricht eine Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="eea25-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eea25-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eea25-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eea25-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eea25-105">DESCRIPTION</span></span>
<span data-ttu-id="eea25-106">Das Suspend-AzureRmAnalysisServicesServer-Cmdlet unterbricht eine Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="eea25-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="eea25-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eea25-107">EXAMPLES</span></span>

### <span data-ttu-id="eea25-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eea25-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="eea25-109">Mit diesem Befehl wird ein aktiver Server mit dem Namen "Testserver" in der testgroup der ResourceGroup angehalten.</span><span class="sxs-lookup"><span data-stu-id="eea25-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="eea25-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eea25-110">PARAMETERS</span></span>

### <span data-ttu-id="eea25-111">-Name</span><span class="sxs-lookup"><span data-stu-id="eea25-111">-Name</span></span>
<span data-ttu-id="eea25-112">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="eea25-112">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eea25-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eea25-113">-PassThru</span></span>
<span data-ttu-id="eea25-114">Gibt die gelöschten Serverdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="eea25-114">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea25-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea25-115">-ResourceGroupName</span></span>
<span data-ttu-id="eea25-116">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="eea25-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eea25-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eea25-117">-Confirm</span></span>
<span data-ttu-id="eea25-118">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="eea25-118">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea25-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea25-119">-WhatIf</span></span>
<span data-ttu-id="eea25-120">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="eea25-120">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea25-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea25-121">CommonParameters</span></span>
<span data-ttu-id="eea25-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea25-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea25-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea25-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea25-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eea25-124">INPUTS</span></span>

## <span data-ttu-id="eea25-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eea25-125">OUTPUTS</span></span>

### <span data-ttu-id="eea25-126">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="eea25-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="eea25-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="eea25-127">NOTES</span></span>
<span data-ttu-id="eea25-128">Alias: Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="eea25-128">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="eea25-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eea25-129">RELATED LINKS</span></span>

[<span data-ttu-id="eea25-130">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="eea25-130">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="eea25-131">Lebenslauf-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="eea25-131">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

