---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/remove-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 541f1a2039f8c7b54a71798432a9f009d57144c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500645"
---
# <span data-ttu-id="30f36-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="30f36-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="30f36-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30f36-102">SYNOPSIS</span></span>
<span data-ttu-id="30f36-103">Löscht eine Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="30f36-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30f36-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30f36-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30f36-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30f36-105">DESCRIPTION</span></span>
<span data-ttu-id="30f36-106">Das Remove-AzureRmAnalysisServicesServer-Cmdlet löscht eine Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="30f36-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="30f36-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30f36-107">EXAMPLES</span></span>

### <span data-ttu-id="30f36-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="30f36-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="30f36-109">Mit diesem Befehl wird der Server mit dem Namen "Testserver" in der testgroup der ResourceGroup entfernt</span><span class="sxs-lookup"><span data-stu-id="30f36-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="30f36-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="30f36-110">PARAMETERS</span></span>

### <span data-ttu-id="30f36-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f36-111">-DefaultProfile</span></span>
<span data-ttu-id="30f36-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="30f36-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30f36-113">-Name</span><span class="sxs-lookup"><span data-stu-id="30f36-113">-Name</span></span>
<span data-ttu-id="30f36-114">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="30f36-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="30f36-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30f36-115">-PassThru</span></span>
<span data-ttu-id="30f36-116">Gibt die gelöschten Serverdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="30f36-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="30f36-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30f36-117">-ResourceGroupName</span></span>
<span data-ttu-id="30f36-118">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="30f36-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="30f36-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="30f36-119">-Confirm</span></span>
<span data-ttu-id="30f36-120">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="30f36-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="30f36-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f36-121">-WhatIf</span></span>
<span data-ttu-id="30f36-122">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="30f36-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="30f36-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f36-123">CommonParameters</span></span>
<span data-ttu-id="30f36-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30f36-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f36-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30f36-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f36-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30f36-126">INPUTS</span></span>

### <span data-ttu-id="30f36-127">Keine</span><span class="sxs-lookup"><span data-stu-id="30f36-127">None</span></span>
<span data-ttu-id="30f36-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="30f36-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30f36-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30f36-129">OUTPUTS</span></span>

### <span data-ttu-id="30f36-130">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="30f36-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="30f36-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="30f36-131">NOTES</span></span>
<span data-ttu-id="30f36-132">Alias: Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="30f36-132">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="30f36-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30f36-133">RELATED LINKS</span></span>

[<span data-ttu-id="30f36-134">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="30f36-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="30f36-135">Neu – AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="30f36-135">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)
