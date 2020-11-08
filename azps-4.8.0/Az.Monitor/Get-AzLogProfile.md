---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: fa8c7768f2fcea53157f1b7bb3d89a5567ecdf2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174640"
---
# <span data-ttu-id="b7c20-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="b7c20-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="b7c20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7c20-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c20-103">Ruft ein Protokoll Profil ab.</span><span class="sxs-lookup"><span data-stu-id="b7c20-103">Gets a log profile.</span></span>

## <span data-ttu-id="b7c20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7c20-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7c20-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7c20-105">DESCRIPTION</span></span>
<span data-ttu-id="b7c20-106">Das Cmdlet " **Get-AzLogProfile** " Ruft ein Protokoll Profil ab.</span><span class="sxs-lookup"><span data-stu-id="b7c20-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="b7c20-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7c20-107">EXAMPLES</span></span>

## <span data-ttu-id="b7c20-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7c20-108">PARAMETERS</span></span>

### <span data-ttu-id="b7c20-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c20-109">-DefaultProfile</span></span>
<span data-ttu-id="b7c20-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b7c20-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c20-111">-Name</span><span class="sxs-lookup"><span data-stu-id="b7c20-111">-Name</span></span>
<span data-ttu-id="b7c20-112">Gibt den Namen des abzurufenden Protokoll Profils an.</span><span class="sxs-lookup"><span data-stu-id="b7c20-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c20-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c20-113">CommonParameters</span></span>
<span data-ttu-id="b7c20-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c20-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c20-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7c20-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c20-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7c20-116">INPUTS</span></span>

### <span data-ttu-id="b7c20-117">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c20-117">System.String</span></span>

## <span data-ttu-id="b7c20-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7c20-118">OUTPUTS</span></span>

### <span data-ttu-id="b7c20-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="b7c20-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="b7c20-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7c20-120">NOTES</span></span>

## <span data-ttu-id="b7c20-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7c20-121">RELATED LINKS</span></span>

[<span data-ttu-id="b7c20-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="b7c20-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="b7c20-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="b7c20-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


