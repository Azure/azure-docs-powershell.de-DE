---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: df53acc047ff0c17b3482f214c357f66ce638efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664683"
---
# <span data-ttu-id="2bc81-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="2bc81-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="2bc81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2bc81-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc81-103">Befehl ' Run-Dokument abrufen '</span><span class="sxs-lookup"><span data-stu-id="2bc81-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bc81-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bc81-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bc81-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bc81-105">DESCRIPTION</span></span>
<span data-ttu-id="2bc81-106">Befehl ' Run-Dokument abrufen '</span><span class="sxs-lookup"><span data-stu-id="2bc81-106">Get run command document.</span></span>

## <span data-ttu-id="2bc81-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bc81-107">EXAMPLES</span></span>

### <span data-ttu-id="2bc81-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2bc81-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="2bc81-109">Ruft ein bestimmtes Ausführungsbefehls Dokument für "RunPowerShellScript" in "westus" ab.</span><span class="sxs-lookup"><span data-stu-id="2bc81-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="2bc81-110">Get-AzureRmVMRunCommandDocument-Standort $loc</span><span class="sxs-lookup"><span data-stu-id="2bc81-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="2bc81-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2bc81-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="2bc81-112">Listet alle verfügbaren Ausführungsbefehle in "westus" auf.</span><span class="sxs-lookup"><span data-stu-id="2bc81-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="2bc81-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bc81-113">PARAMETERS</span></span>

### <span data-ttu-id="2bc81-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="2bc81-114">-CommandId</span></span>
<span data-ttu-id="2bc81-115">Die Befehls-ID.</span><span class="sxs-lookup"><span data-stu-id="2bc81-115">The command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc81-116">-DefaultProfile</span></span>
<span data-ttu-id="2bc81-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2bc81-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bc81-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="2bc81-118">-Location</span></span>
<span data-ttu-id="2bc81-119">Die Position, an der Ausführungsbefehle abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="2bc81-119">The location upon which run commands is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc81-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc81-120">CommonParameters</span></span>
<span data-ttu-id="2bc81-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc81-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc81-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bc81-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc81-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2bc81-123">INPUTS</span></span>

### <span data-ttu-id="2bc81-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2bc81-124">System.String</span></span>

## <span data-ttu-id="2bc81-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2bc81-125">OUTPUTS</span></span>

### <span data-ttu-id="2bc81-126">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="2bc81-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="2bc81-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="2bc81-127">NOTES</span></span>

## <span data-ttu-id="2bc81-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2bc81-128">RELATED LINKS</span></span>
