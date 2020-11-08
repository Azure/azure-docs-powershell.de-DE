---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CEFFEF9F-4500-447E-99F1-FE053AED880A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e5b65a88e41ce08ec1d60bc140828963950f447
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005804"
---
# <span data-ttu-id="b86ed-101">Get-AzureServiceProjectRoleRuntime</span><span class="sxs-lookup"><span data-stu-id="b86ed-101">Get-AzureServiceProjectRoleRuntime</span></span>

## <span data-ttu-id="b86ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b86ed-102">SYNOPSIS</span></span>
<span data-ttu-id="b86ed-103">Rufen Sie die zur Installation in einer Rolle verfügbaren Runtimes ab.</span><span class="sxs-lookup"><span data-stu-id="b86ed-103">Get the runtimes available to install in a role.</span></span>

## <span data-ttu-id="b86ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b86ed-104">SYNTAX</span></span>

```
Get-AzureServiceProjectRoleRuntime [-Runtime <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b86ed-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b86ed-105">DESCRIPTION</span></span>
<span data-ttu-id="b86ed-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b86ed-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b86ed-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b86ed-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b86ed-108">Ruft die zur Installation in einer Rolle verfügbaren Runtimes ab.</span><span class="sxs-lookup"><span data-stu-id="b86ed-108">Gets the runtimes available to install in a role.</span></span>

## <span data-ttu-id="b86ed-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b86ed-109">EXAMPLES</span></span>

## <span data-ttu-id="b86ed-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b86ed-110">PARAMETERS</span></span>

### <span data-ttu-id="b86ed-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="b86ed-111">-Profile</span></span>
<span data-ttu-id="b86ed-112">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b86ed-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b86ed-113">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b86ed-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b86ed-114">-Runtime</span><span class="sxs-lookup"><span data-stu-id="b86ed-114">-Runtime</span></span>
<span data-ttu-id="b86ed-115">Der Name der Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="b86ed-115">The name of the runtime.</span></span>
<span data-ttu-id="b86ed-116">Wenn eine Laufzeit angegeben ist, werden nur die spezifischen Versionen dieser Runtime zurückgegeben, die für die Installation in ihrer Rolle in Windows Azure verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b86ed-116">If a runtime specified, only the specific versions of that runtime available to install in your role in Windows Azure will be returned.</span></span>

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

### <span data-ttu-id="b86ed-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b86ed-117">CommonParameters</span></span>
<span data-ttu-id="b86ed-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b86ed-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b86ed-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b86ed-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b86ed-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b86ed-120">INPUTS</span></span>

## <span data-ttu-id="b86ed-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b86ed-121">OUTPUTS</span></span>

## <span data-ttu-id="b86ed-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="b86ed-122">NOTES</span></span>

## <span data-ttu-id="b86ed-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b86ed-123">RELATED LINKS</span></span>

[<span data-ttu-id="b86ed-124">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="b86ed-124">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="b86ed-125">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="b86ed-125">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="b86ed-126">Satz-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="b86ed-126">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)

[<span data-ttu-id="b86ed-127">Satz-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="b86ed-127">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


