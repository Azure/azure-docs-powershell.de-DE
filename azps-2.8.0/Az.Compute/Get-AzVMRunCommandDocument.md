---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 3b66cdc6574397de7d43dfef0677a5ddac772a31
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652123"
---
# <span data-ttu-id="68ad2-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="68ad2-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="68ad2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="68ad2-103">Rufen Sie ein Ausführungsbefehl-Dokument ab.</span><span class="sxs-lookup"><span data-stu-id="68ad2-103">Get a run command document.</span></span>

## <span data-ttu-id="68ad2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68ad2-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68ad2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="68ad2-106">Rufen Sie ein Ausführungsbefehl-Dokument ab.</span><span class="sxs-lookup"><span data-stu-id="68ad2-106">Get a run command document.</span></span>

## <span data-ttu-id="68ad2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68ad2-107">EXAMPLES</span></span>

### <span data-ttu-id="68ad2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="68ad2-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="68ad2-109">Ruft ein bestimmtes Ausführungsbefehls Dokument für "RunPowerShellScript" in "westus" ab.</span><span class="sxs-lookup"><span data-stu-id="68ad2-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="68ad2-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="68ad2-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="68ad2-111">Listet alle verfügbaren Ausführungsbefehle in "westus" auf.</span><span class="sxs-lookup"><span data-stu-id="68ad2-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="68ad2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="68ad2-112">PARAMETERS</span></span>

### <span data-ttu-id="68ad2-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="68ad2-113">-CommandId</span></span>
<span data-ttu-id="68ad2-114">Die Befehls-ID.</span><span class="sxs-lookup"><span data-stu-id="68ad2-114">The command ID.</span></span>

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

### <span data-ttu-id="68ad2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ad2-115">-DefaultProfile</span></span>
<span data-ttu-id="68ad2-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="68ad2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68ad2-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="68ad2-117">-Location</span></span>
<span data-ttu-id="68ad2-118">Die Position, auf der Ausführungsbefehle abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="68ad2-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="68ad2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ad2-119">CommonParameters</span></span>
<span data-ttu-id="68ad2-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68ad2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ad2-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68ad2-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ad2-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68ad2-122">INPUTS</span></span>

### <span data-ttu-id="68ad2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="68ad2-123">System.String</span></span>

## <span data-ttu-id="68ad2-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68ad2-124">OUTPUTS</span></span>

### <span data-ttu-id="68ad2-125">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="68ad2-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="68ad2-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="68ad2-126">NOTES</span></span>

## <span data-ttu-id="68ad2-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68ad2-127">RELATED LINKS</span></span>
