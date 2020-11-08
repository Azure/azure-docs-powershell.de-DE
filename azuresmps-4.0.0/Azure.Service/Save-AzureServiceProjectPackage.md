---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9445B7FA-FC72-4F71-BD44-8AA55BE9BA0E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d2a3dbabb5bbe78ed571806aa69b9d79d4782b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005666"
---
# <span data-ttu-id="d98f5-101">Save-AzureServiceProjectPackage</span><span class="sxs-lookup"><span data-stu-id="d98f5-101">Save-AzureServiceProjectPackage</span></span>

## <span data-ttu-id="d98f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d98f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d98f5-103">Verpackt das Dienstprojekt in das Azure Cloud-Paket.</span><span class="sxs-lookup"><span data-stu-id="d98f5-103">Packages the service project into Azure cloud package.</span></span>

## <span data-ttu-id="d98f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d98f5-104">SYNTAX</span></span>

```
Save-AzureServiceProjectPackage [-Local] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d98f5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d98f5-105">DESCRIPTION</span></span>
<span data-ttu-id="d98f5-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d98f5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d98f5-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d98f5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d98f5-108">Das Cmdlet **Save-AzureServiceProjectPackage** verpackt das Dienstprojekt in ein Azure Cloud-Paket (\*. cspkg).</span><span class="sxs-lookup"><span data-stu-id="d98f5-108">The **Save-AzureServiceProjectPackage** cmdlet packages the service project into an Azure cloud package (\*.cspkg).</span></span>

## <span data-ttu-id="d98f5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d98f5-109">EXAMPLES</span></span>

### <span data-ttu-id="d98f5-110">Beispiel 1: Erstellen eines Dienstprojekt Pakets</span><span class="sxs-lookup"><span data-stu-id="d98f5-110">Example 1: Create a service project package</span></span>
```
PS C:\> Save-AzureServiceProjectPackage
```

<span data-ttu-id="d98f5-111">In diesem Beispiel wird ein \*. cspgk für ein Dienstprojekt mit dem Namen MyAzureServiceProject erstellt.</span><span class="sxs-lookup"><span data-stu-id="d98f5-111">This example creates a \*.cspgk for a service project named MyAzureServiceProject.</span></span>

## <span data-ttu-id="d98f5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d98f5-112">PARAMETERS</span></span>

### <span data-ttu-id="d98f5-113">-Lokal</span><span class="sxs-lookup"><span data-stu-id="d98f5-113">-Local</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d98f5-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="d98f5-114">-Profile</span></span>
<span data-ttu-id="d98f5-115">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d98f5-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d98f5-116">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d98f5-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d98f5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d98f5-117">CommonParameters</span></span>
<span data-ttu-id="d98f5-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d98f5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d98f5-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d98f5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d98f5-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d98f5-120">INPUTS</span></span>

## <span data-ttu-id="d98f5-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d98f5-121">OUTPUTS</span></span>

## <span data-ttu-id="d98f5-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="d98f5-122">NOTES</span></span>

## <span data-ttu-id="d98f5-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d98f5-123">RELATED LINKS</span></span>

[<span data-ttu-id="d98f5-124">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="d98f5-124">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


