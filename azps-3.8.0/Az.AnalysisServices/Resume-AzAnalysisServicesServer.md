---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: 3614c62af825b109b224d231d89dda315a7e2616
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996752"
---
# <span data-ttu-id="d7477-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d7477-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="d7477-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7477-102">SYNOPSIS</span></span>
<span data-ttu-id="d7477-103">Setzt eine Instanz des Analysis Services-Servers fort</span><span class="sxs-lookup"><span data-stu-id="d7477-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="d7477-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7477-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7477-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7477-105">DESCRIPTION</span></span>
<span data-ttu-id="d7477-106">Das Resume-AzAnalysisServicesServer-Cmdlet setzt eine Instanz des Analysis Services-Servers fort</span><span class="sxs-lookup"><span data-stu-id="d7477-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="d7477-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7477-107">EXAMPLES</span></span>

### <span data-ttu-id="d7477-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d7477-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="d7477-109">Mit diesem Befehl wird ein angehaltener Server mit dem Namen "Testserver" in der testgroup der ResourceGroup fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d7477-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="d7477-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7477-110">PARAMETERS</span></span>

### <span data-ttu-id="d7477-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7477-111">-DefaultProfile</span></span>
<span data-ttu-id="d7477-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7477-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7477-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d7477-113">-Name</span></span>
<span data-ttu-id="d7477-114">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="d7477-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="d7477-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7477-115">-PassThru</span></span>
<span data-ttu-id="d7477-116">Gibt die gelöschten Serverdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d7477-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="d7477-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7477-117">-ResourceGroupName</span></span>
<span data-ttu-id="d7477-118">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="d7477-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="d7477-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7477-119">-Confirm</span></span>
<span data-ttu-id="d7477-120">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="d7477-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="d7477-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7477-121">-WhatIf</span></span>
<span data-ttu-id="d7477-122">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="d7477-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="d7477-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7477-123">CommonParameters</span></span>
<span data-ttu-id="d7477-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7477-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7477-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7477-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7477-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7477-126">INPUTS</span></span>

### <span data-ttu-id="d7477-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d7477-127">System.String</span></span>

## <span data-ttu-id="d7477-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7477-128">OUTPUTS</span></span>

### <span data-ttu-id="d7477-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d7477-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="d7477-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7477-130">NOTES</span></span>
<span data-ttu-id="d7477-131">Alias: Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="d7477-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="d7477-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7477-132">RELATED LINKS</span></span>

[<span data-ttu-id="d7477-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d7477-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="d7477-134">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d7477-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
