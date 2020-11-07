---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 45d051e5fc2fe750f58dc6400a037960b7eb9c7c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844571"
---
# <span data-ttu-id="ddb8b-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="ddb8b-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="ddb8b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ddb8b-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb8b-103">Befehl ' Run-Dokument abrufen '</span><span class="sxs-lookup"><span data-stu-id="ddb8b-103">Get run command document.</span></span>

## <span data-ttu-id="ddb8b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddb8b-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddb8b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ddb8b-105">DESCRIPTION</span></span>
<span data-ttu-id="ddb8b-106">Befehl ' Run-Dokument abrufen '</span><span class="sxs-lookup"><span data-stu-id="ddb8b-106">Get run command document.</span></span>

## <span data-ttu-id="ddb8b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ddb8b-107">EXAMPLES</span></span>

### <span data-ttu-id="ddb8b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ddb8b-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="ddb8b-109">Ruft ein bestimmtes Ausführungsbefehls Dokument für "RunPowerShellScript" in "westus" ab.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="ddb8b-110">Get-AzVMRunCommandDocument-Standort $loc</span><span class="sxs-lookup"><span data-stu-id="ddb8b-110">Get-AzVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="ddb8b-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ddb8b-111">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="ddb8b-112">Listet alle verfügbaren Ausführungsbefehle in "westus" auf.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="ddb8b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddb8b-113">PARAMETERS</span></span>

### <span data-ttu-id="ddb8b-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="ddb8b-114">-CommandId</span></span>
<span data-ttu-id="ddb8b-115">Die Befehls-ID.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-115">The command id.</span></span>

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

### <span data-ttu-id="ddb8b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb8b-116">-DefaultProfile</span></span>
<span data-ttu-id="ddb8b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddb8b-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="ddb8b-118">-Location</span></span>
<span data-ttu-id="ddb8b-119">Die Position, an der Ausführungsbefehle abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="ddb8b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb8b-120">CommonParameters</span></span>
<span data-ttu-id="ddb8b-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb8b-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddb8b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb8b-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ddb8b-123">INPUTS</span></span>

### <span data-ttu-id="ddb8b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ddb8b-124">System.String</span></span>

## <span data-ttu-id="ddb8b-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ddb8b-125">OUTPUTS</span></span>

### <span data-ttu-id="ddb8b-126">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="ddb8b-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="ddb8b-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="ddb8b-127">NOTES</span></span>

## <span data-ttu-id="ddb8b-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ddb8b-128">RELATED LINKS</span></span>

