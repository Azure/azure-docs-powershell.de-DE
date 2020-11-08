---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: 9076df0ae023539560b690723dd9abc92d922e45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176687"
---
# <span data-ttu-id="ad1f3-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ad1f3-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="ad1f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad1f3-102">SYNOPSIS</span></span>
<span data-ttu-id="ad1f3-103">Löscht eine Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="ad1f3-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="ad1f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad1f3-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad1f3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad1f3-105">DESCRIPTION</span></span>
<span data-ttu-id="ad1f3-106">Das Remove-AzAnalysisServicesServer-Cmdlet löscht eine Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="ad1f3-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="ad1f3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad1f3-107">EXAMPLES</span></span>

### <span data-ttu-id="ad1f3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ad1f3-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="ad1f3-109">Mit diesem Befehl wird der Server mit dem Namen "Testserver" in der testgroup der ResourceGroup entfernt</span><span class="sxs-lookup"><span data-stu-id="ad1f3-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="ad1f3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad1f3-110">PARAMETERS</span></span>

### <span data-ttu-id="ad1f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad1f3-111">-DefaultProfile</span></span>
<span data-ttu-id="ad1f3-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad1f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad1f3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ad1f3-113">-Name</span></span>
<span data-ttu-id="ad1f3-114">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="ad1f3-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="ad1f3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad1f3-115">-PassThru</span></span>
<span data-ttu-id="ad1f3-116">Gibt die gelöschten Serverdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ad1f3-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="ad1f3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad1f3-117">-ResourceGroupName</span></span>
<span data-ttu-id="ad1f3-118">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="ad1f3-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="ad1f3-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ad1f3-119">-Confirm</span></span>
<span data-ttu-id="ad1f3-120">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="ad1f3-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="ad1f3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad1f3-121">-WhatIf</span></span>
<span data-ttu-id="ad1f3-122">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="ad1f3-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="ad1f3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad1f3-123">CommonParameters</span></span>
<span data-ttu-id="ad1f3-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad1f3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad1f3-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad1f3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad1f3-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad1f3-126">INPUTS</span></span>

### <span data-ttu-id="ad1f3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ad1f3-127">System.String</span></span>

## <span data-ttu-id="ad1f3-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad1f3-128">OUTPUTS</span></span>

### <span data-ttu-id="ad1f3-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ad1f3-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="ad1f3-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad1f3-130">NOTES</span></span>
<span data-ttu-id="ad1f3-131">Alias: Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="ad1f3-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="ad1f3-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad1f3-132">RELATED LINKS</span></span>

[<span data-ttu-id="ad1f3-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ad1f3-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="ad1f3-134">Neu – AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ad1f3-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)
