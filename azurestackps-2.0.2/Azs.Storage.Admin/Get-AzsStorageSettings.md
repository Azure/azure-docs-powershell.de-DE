---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006957"
---
# <span data-ttu-id="bdb29-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="bdb29-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="bdb29-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bdb29-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb29-103">Gibt die Einstellungen für den Speicherressourcen Anbieter zurück.</span><span class="sxs-lookup"><span data-stu-id="bdb29-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="bdb29-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdb29-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdb29-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdb29-105">DESCRIPTION</span></span>
<span data-ttu-id="bdb29-106">Gibt die Einstellungen für den Speicherressourcen Anbieter zurück.</span><span class="sxs-lookup"><span data-stu-id="bdb29-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="bdb29-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdb29-107">EXAMPLES</span></span>

### <span data-ttu-id="bdb29-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="bdb29-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="bdb29-109">Abrufen der Speichereinstellungen</span><span class="sxs-lookup"><span data-stu-id="bdb29-109">Get the storage settings.</span></span>

## <span data-ttu-id="bdb29-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdb29-110">PARAMETERS</span></span>

### <span data-ttu-id="bdb29-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb29-111">-DefaultProfile</span></span>
<span data-ttu-id="bdb29-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bdb29-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdb29-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="bdb29-113">-Location</span></span>
<span data-ttu-id="bdb29-114">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="bdb29-114">Resource location.</span></span>

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

### <span data-ttu-id="bdb29-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="bdb29-115">-SubscriptionId</span></span>
<span data-ttu-id="bdb29-116">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="bdb29-116">Subscription Id.</span></span>

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

### <span data-ttu-id="bdb29-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb29-117">CommonParameters</span></span>
<span data-ttu-id="bdb29-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdb29-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb29-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdb29-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb29-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bdb29-120">INPUTS</span></span>

## <span data-ttu-id="bdb29-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bdb29-121">OUTPUTS</span></span>

### <span data-ttu-id="bdb29-122">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="bdb29-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="bdb29-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="bdb29-123">NOTES</span></span>

## <span data-ttu-id="bdb29-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bdb29-124">RELATED LINKS</span></span>

