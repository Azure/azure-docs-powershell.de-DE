---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: fd52bf58e3e240f65be88d8f9f682b2543e1f458
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665401"
---
# <span data-ttu-id="e4500-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="e4500-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="e4500-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e4500-102">SYNOPSIS</span></span>
<span data-ttu-id="e4500-103">Befehl ' Run-Dokument abrufen '</span><span class="sxs-lookup"><span data-stu-id="e4500-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4500-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4500-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4500-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4500-105">DESCRIPTION</span></span>
<span data-ttu-id="e4500-106">Befehl ' Run-Dokument abrufen '</span><span class="sxs-lookup"><span data-stu-id="e4500-106">Get run command document.</span></span>

## <span data-ttu-id="e4500-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4500-107">EXAMPLES</span></span>

### <span data-ttu-id="e4500-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e4500-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="e4500-109">Ruft ein bestimmtes Ausführungsbefehls Dokument für "RunPowerShellScript" in "westus" ab.</span><span class="sxs-lookup"><span data-stu-id="e4500-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="e4500-110">Get-AzureRmVMRunCommandDocument-Standort $loc</span><span class="sxs-lookup"><span data-stu-id="e4500-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="e4500-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e4500-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="e4500-112">Listet alle verfügbaren Ausführungsbefehle in "westus" auf.</span><span class="sxs-lookup"><span data-stu-id="e4500-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="e4500-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4500-113">PARAMETERS</span></span>

### <span data-ttu-id="e4500-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="e4500-114">-CommandId</span></span>
<span data-ttu-id="e4500-115">Die Befehls-ID.</span><span class="sxs-lookup"><span data-stu-id="e4500-115">The command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4500-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4500-116">-DefaultProfile</span></span>
<span data-ttu-id="e4500-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e4500-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4500-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="e4500-118">-Location</span></span>
<span data-ttu-id="e4500-119">Die Position, an der Ausführungsbefehle abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="e4500-119">The location upon which run commands is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4500-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4500-120">CommonParameters</span></span>
<span data-ttu-id="e4500-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4500-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4500-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4500-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4500-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e4500-123">INPUTS</span></span>

### <span data-ttu-id="e4500-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e4500-124">System.String</span></span>

## <span data-ttu-id="e4500-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e4500-125">OUTPUTS</span></span>

### <span data-ttu-id="e4500-126">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="e4500-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="e4500-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4500-127">NOTES</span></span>

## <span data-ttu-id="e4500-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e4500-128">RELATED LINKS</span></span>

