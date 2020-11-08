---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1D433BD2-4604-474B-A2DA-BC80EE935E5C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ffbe5ae961c1733be68c902a9657b200cba0a5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005819"
---
# <span data-ttu-id="7f289-101">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="7f289-101">Get-AzureSBNamespace</span></span>

## <span data-ttu-id="7f289-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f289-102">SYNOPSIS</span></span>
<span data-ttu-id="7f289-103">Ruft den Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="7f289-103">Gets the namespace.</span></span>


## <span data-ttu-id="7f289-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f289-104">SYNTAX</span></span>

```
Get-AzureSBNamespace [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7f289-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f289-105">DESCRIPTION</span></span>
<span data-ttu-id="7f289-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7f289-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7f289-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7f289-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7f289-108">Das Cmdlet " **Get-AzureSBNamespace** " gibt die Service Bus-Dienst-Namespaces zurück, die dem aktuellen Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7f289-108">The **Get-AzureSBNamespace** cmdlet returns the Service Bus service namespaces associated with the current subscription.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="7f289-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f289-109">EXAMPLES</span></span>

### <span data-ttu-id="7f289-110">Beispiel 1: Abrufen des ServiceBus-Namespaces</span><span class="sxs-lookup"><span data-stu-id="7f289-110">Example 1: Get the Service Bus namespace</span></span>
```
PS C:\> Get-AzureSBNamespace
```

<span data-ttu-id="7f289-111">In diesem Beispiel werden die servicebusdienst-Namespaces abgerufen, die dem aktuellen Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7f289-111">This example gets the Service Bus service namespaces associated with the current subscription.</span></span>

## <span data-ttu-id="7f289-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f289-112">PARAMETERS</span></span>

### <span data-ttu-id="7f289-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7f289-113">-Name</span></span>
<span data-ttu-id="7f289-114">Gibt den Namen eines ServiceBus-Namespace an, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f289-114">Specifies the name of a Service Bus namespace to look for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f289-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="7f289-115">-Profile</span></span>
<span data-ttu-id="7f289-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7f289-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7f289-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7f289-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7f289-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f289-118">CommonParameters</span></span>
<span data-ttu-id="7f289-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f289-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f289-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f289-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f289-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f289-121">INPUTS</span></span>

## <span data-ttu-id="7f289-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f289-122">OUTPUTS</span></span>

## <span data-ttu-id="7f289-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f289-123">NOTES</span></span>

## <span data-ttu-id="7f289-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f289-124">RELATED LINKS</span></span>

[<span data-ttu-id="7f289-125">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="7f289-125">Get-AzureSBLocation</span></span>](./Get-AzureSBLocation.md)


