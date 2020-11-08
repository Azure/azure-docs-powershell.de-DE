---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180131"
---
# <span data-ttu-id="e1d5a-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="e1d5a-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="e1d5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d5a-103">Rufen Sie ein Ausführungsbefehl-Dokument ab.</span><span class="sxs-lookup"><span data-stu-id="e1d5a-103">Get a run command document.</span></span>

## <span data-ttu-id="e1d5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1d5a-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1d5a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1d5a-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d5a-106">Rufen Sie ein Ausführungsbefehl-Dokument ab.</span><span class="sxs-lookup"><span data-stu-id="e1d5a-106">Get a run command document.</span></span>

## <span data-ttu-id="e1d5a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1d5a-107">EXAMPLES</span></span>

### <span data-ttu-id="e1d5a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1d5a-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="e1d5a-109">Ruft ein bestimmtes Ausführungsbefehls Dokument für "RunPowerShellScript" in "westus" ab.</span><span class="sxs-lookup"><span data-stu-id="e1d5a-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="e1d5a-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e1d5a-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="e1d5a-111">Listet alle verfügbaren Ausführungsbefehle in "westus" auf.</span><span class="sxs-lookup"><span data-stu-id="e1d5a-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="e1d5a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1d5a-112">PARAMETERS</span></span>

### <span data-ttu-id="e1d5a-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="e1d5a-113">-CommandId</span></span>
<span data-ttu-id="e1d5a-114">Die Befehls-ID.</span><span class="sxs-lookup"><span data-stu-id="e1d5a-114">The command ID.</span></span>

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

### <span data-ttu-id="e1d5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d5a-115">-DefaultProfile</span></span>
<span data-ttu-id="e1d5a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1d5a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d5a-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="e1d5a-117">-Location</span></span>
<span data-ttu-id="e1d5a-118">Die Position, auf der Ausführungsbefehle abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="e1d5a-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="e1d5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d5a-119">CommonParameters</span></span>
<span data-ttu-id="e1d5a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d5a-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1d5a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d5a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1d5a-122">INPUTS</span></span>

### <span data-ttu-id="e1d5a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e1d5a-123">System.String</span></span>

## <span data-ttu-id="e1d5a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1d5a-124">OUTPUTS</span></span>

### <span data-ttu-id="e1d5a-125">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="e1d5a-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="e1d5a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1d5a-126">NOTES</span></span>

## <span data-ttu-id="e1d5a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1d5a-127">RELATED LINKS</span></span>
