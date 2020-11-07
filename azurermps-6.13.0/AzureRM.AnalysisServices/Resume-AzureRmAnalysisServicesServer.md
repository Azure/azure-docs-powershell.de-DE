---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/resume-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 28a89c40fcfd470d20d9b4423d40c38b43624edd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662335"
---
# <span data-ttu-id="4e2f3-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4e2f3-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="4e2f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="4e2f3-103">Setzt eine Instanz des Analysis Services-Servers fort</span><span class="sxs-lookup"><span data-stu-id="4e2f3-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e2f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e2f3-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e2f3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e2f3-105">DESCRIPTION</span></span>
<span data-ttu-id="4e2f3-106">Das Resume-AzureRmAnalysisServicesServer-Cmdlet setzt eine Instanz des Analysis Services-Servers fort</span><span class="sxs-lookup"><span data-stu-id="4e2f3-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="4e2f3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e2f3-107">EXAMPLES</span></span>

### <span data-ttu-id="4e2f3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e2f3-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="4e2f3-109">Mit diesem Befehl wird ein angehaltener Server mit dem Namen "Testserver" in der testgroup der ResourceGroup fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4e2f3-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="4e2f3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e2f3-110">PARAMETERS</span></span>

### <span data-ttu-id="4e2f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e2f3-111">-DefaultProfile</span></span>
<span data-ttu-id="4e2f3-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e2f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e2f3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4e2f3-113">-Name</span></span>
<span data-ttu-id="4e2f3-114">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="4e2f3-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e2f3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e2f3-115">-PassThru</span></span>
<span data-ttu-id="4e2f3-116">Gibt die gelöschten Serverdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4e2f3-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="4e2f3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e2f3-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e2f3-118">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="4e2f3-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e2f3-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4e2f3-119">-Confirm</span></span>
<span data-ttu-id="4e2f3-120">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="4e2f3-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4e2f3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e2f3-121">-WhatIf</span></span>
<span data-ttu-id="4e2f3-122">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="4e2f3-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4e2f3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e2f3-123">CommonParameters</span></span>
<span data-ttu-id="4e2f3-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e2f3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e2f3-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e2f3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e2f3-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e2f3-126">INPUTS</span></span>

### <span data-ttu-id="4e2f3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4e2f3-127">System.String</span></span>

## <span data-ttu-id="4e2f3-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e2f3-128">OUTPUTS</span></span>

### <span data-ttu-id="4e2f3-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4e2f3-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="4e2f3-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e2f3-130">NOTES</span></span>
<span data-ttu-id="4e2f3-131">Alias: Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="4e2f3-131">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="4e2f3-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e2f3-132">RELATED LINKS</span></span>

[<span data-ttu-id="4e2f3-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4e2f3-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="4e2f3-134">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4e2f3-134">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
