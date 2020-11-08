---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006755"
---
# <span data-ttu-id="1036a-101">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="1036a-101">Get-AzureStorSimpleResourceContext</span></span>

## <span data-ttu-id="1036a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1036a-102">SYNOPSIS</span></span>
<span data-ttu-id="1036a-103">Ruft den aktuellen Ressourcenkontext ab.</span><span class="sxs-lookup"><span data-stu-id="1036a-103">Gets the current resource context.</span></span>

## <span data-ttu-id="1036a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1036a-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1036a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1036a-105">DESCRIPTION</span></span>
<span data-ttu-id="1036a-106">Das Cmdlet " **Get-AzureStorSimpleResourceContext** " Ruft den aktuellen Ressourcenkontext ab.</span><span class="sxs-lookup"><span data-stu-id="1036a-106">The **Get-AzureStorSimpleResourceContext** cmdlet gets the current resource context.</span></span>

## <span data-ttu-id="1036a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1036a-107">EXAMPLES</span></span>

### <span data-ttu-id="1036a-108">Beispiel 1: Abrufen des aktuellen Kontexts</span><span class="sxs-lookup"><span data-stu-id="1036a-108">Example 1: Get the current context</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

<span data-ttu-id="1036a-109">Mit dem ersten Befehl wird der aktuelle Kontext mithilfe des Cmdlets **Select-AzureStorSimpleResource** auf die Ressource mit dem Namen "Contoso63-Tsqa" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1036a-109">The first command sets the current context to be the resource named Contoso63-Tsqa by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>

<span data-ttu-id="1036a-110">Der zweite Befehl ruft den aktuellen Ressourcenkontext ab.</span><span class="sxs-lookup"><span data-stu-id="1036a-110">The second command gets the current resource context.</span></span>

### <span data-ttu-id="1036a-111">Beispiel 2: Versuch, den aktuellen Kontext abzurufen</span><span class="sxs-lookup"><span data-stu-id="1036a-111">Example 2: Attempt to get the current context</span></span>
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

<span data-ttu-id="1036a-112">Mit diesem Befehl wird der aktuelle Kontext abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1036a-112">This command gets the current context.</span></span>
<span data-ttu-id="1036a-113">In diesem Beispiel wurde kein Kontext gesetzt.</span><span class="sxs-lookup"><span data-stu-id="1036a-113">In this example, no context has been set.</span></span>
<span data-ttu-id="1036a-114">Der Befehl gibt eine Meldung zurück, die das Problem erläutert.</span><span class="sxs-lookup"><span data-stu-id="1036a-114">The command returns a message that explains the problem.</span></span>

## <span data-ttu-id="1036a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1036a-115">PARAMETERS</span></span>

### <span data-ttu-id="1036a-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="1036a-116">-Profile</span></span>
<span data-ttu-id="1036a-117">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="1036a-117">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1036a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1036a-118">CommonParameters</span></span>
<span data-ttu-id="1036a-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1036a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1036a-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1036a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1036a-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1036a-121">INPUTS</span></span>

### <span data-ttu-id="1036a-122">Keine</span><span class="sxs-lookup"><span data-stu-id="1036a-122">None</span></span>

## <span data-ttu-id="1036a-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1036a-123">OUTPUTS</span></span>

### <span data-ttu-id="1036a-124">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="1036a-124">StorSimpleResourceContext</span></span>
<span data-ttu-id="1036a-125">Dieses Cmdlet gibt ein **resourcecontext** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="1036a-125">This cmdlet returns a **ResourceContext** object.</span></span>

## <span data-ttu-id="1036a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="1036a-126">NOTES</span></span>

## <span data-ttu-id="1036a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1036a-127">RELATED LINKS</span></span>

[<span data-ttu-id="1036a-128">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="1036a-128">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="1036a-129">SELECT-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="1036a-129">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


