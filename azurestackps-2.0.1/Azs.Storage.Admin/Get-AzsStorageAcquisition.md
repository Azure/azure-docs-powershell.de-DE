---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageacquisition
schema: 2.0.0
ms.openlocfilehash: 098c268d3894d85efe0e17618b5d7ec46b82b0f2
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005467"
---
# <span data-ttu-id="2f929-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="2f929-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="2f929-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f929-102">SYNOPSIS</span></span>
<span data-ttu-id="2f929-103">Gibt eine Liste der BLOB-Akquisitionen zurück.</span><span class="sxs-lookup"><span data-stu-id="2f929-103">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="2f929-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f929-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f929-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f929-105">DESCRIPTION</span></span>
<span data-ttu-id="2f929-106">Gibt eine Liste der BLOB-Akquisitionen zurück.</span><span class="sxs-lookup"><span data-stu-id="2f929-106">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="2f929-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f929-107">EXAMPLES</span></span>

### <span data-ttu-id="2f929-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="2f929-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAcquisition
```

<span data-ttu-id="2f929-109">Rufen Sie die Liste der BLOB-Akquisitionen.</span><span class="sxs-lookup"><span data-stu-id="2f929-109">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="2f929-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f929-110">PARAMETERS</span></span>

### <span data-ttu-id="2f929-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f929-111">-DefaultProfile</span></span>
<span data-ttu-id="2f929-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f929-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f929-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="2f929-113">-Location</span></span>
<span data-ttu-id="2f929-114">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="2f929-114">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f929-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2f929-115">-SubscriptionId</span></span>
<span data-ttu-id="2f929-116">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="2f929-116">Subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f929-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f929-117">CommonParameters</span></span>
<span data-ttu-id="2f929-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f929-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f929-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f929-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f929-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f929-120">INPUTS</span></span>

## <span data-ttu-id="2f929-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f929-121">OUTPUTS</span></span>

### <span data-ttu-id="2f929-122">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IAcquisition</span><span class="sxs-lookup"><span data-stu-id="2f929-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IAcquisition</span></span>



## <span data-ttu-id="2f929-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f929-123">NOTES</span></span>

## <span data-ttu-id="2f929-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f929-124">RELATED LINKS</span></span>

