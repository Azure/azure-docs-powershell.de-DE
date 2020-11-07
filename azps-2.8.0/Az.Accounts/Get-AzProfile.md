---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 937683c8592bb814b7f6a6262ef095cbd8252c78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658456"
---
# <span data-ttu-id="57050-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="57050-101">Get-AzProfile</span></span>

## <span data-ttu-id="57050-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57050-102">SYNOPSIS</span></span>
<span data-ttu-id="57050-103">Rufen Sie die von installierten Modulen unterstützten Dienstprofile ab.</span><span class="sxs-lookup"><span data-stu-id="57050-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="57050-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57050-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="57050-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57050-105">DESCRIPTION</span></span>
<span data-ttu-id="57050-106">Rufen Sie die von installierten Modulen unterstützten Dienstprofile ab.</span><span class="sxs-lookup"><span data-stu-id="57050-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="57050-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57050-107">EXAMPLES</span></span>

### <span data-ttu-id="57050-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="57050-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="57050-109">Abrufen des vom keyvault-Modul unterstützten Dienstprofils</span><span class="sxs-lookup"><span data-stu-id="57050-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="57050-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="57050-110">PARAMETERS</span></span>

### <span data-ttu-id="57050-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="57050-111">-ListAvailable</span></span>
<span data-ttu-id="57050-112">Auflisten aller von installierten Modulen unterstützten Dienstprofile</span><span class="sxs-lookup"><span data-stu-id="57050-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="57050-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="57050-113">-ModuleName</span></span>
<span data-ttu-id="57050-114">Der Name des zu überprüfenden Moduls</span><span class="sxs-lookup"><span data-stu-id="57050-114">The name of the module to check</span></span>

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

### <span data-ttu-id="57050-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57050-115">CommonParameters</span></span>
<span data-ttu-id="57050-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57050-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57050-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57050-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57050-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57050-118">INPUTS</span></span>

### <span data-ttu-id="57050-119">Keine</span><span class="sxs-lookup"><span data-stu-id="57050-119">None</span></span>

## <span data-ttu-id="57050-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57050-120">OUTPUTS</span></span>

### <span data-ttu-id="57050-121">Microsoft. Azure. Commands. profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="57050-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="57050-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="57050-122">NOTES</span></span>

## <span data-ttu-id="57050-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57050-123">RELATED LINKS</span></span>
