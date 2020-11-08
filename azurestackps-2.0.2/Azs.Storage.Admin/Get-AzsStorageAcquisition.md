---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageacquisition
schema: 2.0.0
ms.openlocfilehash: 098c268d3894d85efe0e17618b5d7ec46b82b0f2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007051"
---
# <span data-ttu-id="f1892-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="f1892-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="f1892-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1892-102">SYNOPSIS</span></span>
<span data-ttu-id="f1892-103">Gibt eine Liste der BLOB-Akquisitionen zurück.</span><span class="sxs-lookup"><span data-stu-id="f1892-103">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="f1892-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1892-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1892-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1892-105">DESCRIPTION</span></span>
<span data-ttu-id="f1892-106">Gibt eine Liste der BLOB-Akquisitionen zurück.</span><span class="sxs-lookup"><span data-stu-id="f1892-106">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="f1892-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1892-107">EXAMPLES</span></span>

### <span data-ttu-id="f1892-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="f1892-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAcquisition
```

<span data-ttu-id="f1892-109">Rufen Sie die Liste der BLOB-Akquisitionen.</span><span class="sxs-lookup"><span data-stu-id="f1892-109">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="f1892-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1892-110">PARAMETERS</span></span>

### <span data-ttu-id="f1892-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1892-111">-DefaultProfile</span></span>
<span data-ttu-id="f1892-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1892-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1892-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="f1892-113">-Location</span></span>
<span data-ttu-id="f1892-114">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="f1892-114">Resource location.</span></span>

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

### <span data-ttu-id="f1892-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f1892-115">-SubscriptionId</span></span>
<span data-ttu-id="f1892-116">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="f1892-116">Subscription Id.</span></span>

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

### <span data-ttu-id="f1892-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1892-117">CommonParameters</span></span>
<span data-ttu-id="f1892-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1892-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1892-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1892-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1892-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1892-120">INPUTS</span></span>

## <span data-ttu-id="f1892-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1892-121">OUTPUTS</span></span>

### <span data-ttu-id="f1892-122">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IAcquisition</span><span class="sxs-lookup"><span data-stu-id="f1892-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IAcquisition</span></span>



## <span data-ttu-id="f1892-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1892-123">NOTES</span></span>

## <span data-ttu-id="f1892-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1892-124">RELATED LINKS</span></span>

