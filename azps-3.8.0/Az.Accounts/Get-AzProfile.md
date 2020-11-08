---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 165a85f48bc39608bd636073b4b12427e0a81bf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003221"
---
# <span data-ttu-id="c2388-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="c2388-101">Get-AzProfile</span></span>

## <span data-ttu-id="c2388-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2388-102">SYNOPSIS</span></span>
<span data-ttu-id="c2388-103">Rufen Sie die von installierten Modulen unterstützten Dienstprofile ab.</span><span class="sxs-lookup"><span data-stu-id="c2388-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="c2388-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2388-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="c2388-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2388-105">DESCRIPTION</span></span>
<span data-ttu-id="c2388-106">Rufen Sie die von installierten Modulen unterstützten Dienstprofile ab.</span><span class="sxs-lookup"><span data-stu-id="c2388-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="c2388-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2388-107">EXAMPLES</span></span>

### <span data-ttu-id="c2388-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2388-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="c2388-109">Abrufen des vom keyvault-Modul unterstützten Dienstprofils</span><span class="sxs-lookup"><span data-stu-id="c2388-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="c2388-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2388-110">PARAMETERS</span></span>

### <span data-ttu-id="c2388-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="c2388-111">-ListAvailable</span></span>
<span data-ttu-id="c2388-112">Auflisten aller von installierten Modulen unterstützten Dienstprofile</span><span class="sxs-lookup"><span data-stu-id="c2388-112">List all service profiles supported by installed modules</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2388-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="c2388-113">-ModuleName</span></span>
<span data-ttu-id="c2388-114">Der Name des zu überprüfenden Moduls</span><span class="sxs-lookup"><span data-stu-id="c2388-114">The name of the module to check</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2388-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2388-115">CommonParameters</span></span>
<span data-ttu-id="c2388-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2388-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2388-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2388-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2388-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2388-118">INPUTS</span></span>

### <span data-ttu-id="c2388-119">Keine</span><span class="sxs-lookup"><span data-stu-id="c2388-119">None</span></span>

## <span data-ttu-id="c2388-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2388-120">OUTPUTS</span></span>

### <span data-ttu-id="c2388-121">Microsoft. Azure. Commands. profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="c2388-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="c2388-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2388-122">NOTES</span></span>

## <span data-ttu-id="c2388-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2388-123">RELATED LINKS</span></span>
