---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: d541c943c8dc9779cdf340440078ca2fd2fb36e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841055"
---
# <span data-ttu-id="0f7aa-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="0f7aa-101">Get-AzProfile</span></span>

## <span data-ttu-id="0f7aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f7aa-102">SYNOPSIS</span></span>
<span data-ttu-id="0f7aa-103">Rufen Sie die von installierten Modulen unterstützten Dienstprofile ab.</span><span class="sxs-lookup"><span data-stu-id="0f7aa-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="0f7aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f7aa-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="0f7aa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f7aa-105">DESCRIPTION</span></span>
<span data-ttu-id="0f7aa-106">Rufen Sie die von installierten Modulen unterstützten Dienstprofile ab.</span><span class="sxs-lookup"><span data-stu-id="0f7aa-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="0f7aa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f7aa-107">EXAMPLES</span></span>

### <span data-ttu-id="0f7aa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f7aa-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="0f7aa-109">Abrufen des vom keyvault-Modul unterstützten Dienstprofils</span><span class="sxs-lookup"><span data-stu-id="0f7aa-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="0f7aa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f7aa-110">PARAMETERS</span></span>

### <span data-ttu-id="0f7aa-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="0f7aa-111">-ListAvailable</span></span>
<span data-ttu-id="0f7aa-112">Auflisten aller von installierten Modulen unterstützten Dienstprofile</span><span class="sxs-lookup"><span data-stu-id="0f7aa-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="0f7aa-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="0f7aa-113">-ModuleName</span></span>
<span data-ttu-id="0f7aa-114">Der Name des zu überprüfenden Moduls</span><span class="sxs-lookup"><span data-stu-id="0f7aa-114">The name of the module to check</span></span>

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

### <span data-ttu-id="0f7aa-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f7aa-115">CommonParameters</span></span>
<span data-ttu-id="0f7aa-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f7aa-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f7aa-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f7aa-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f7aa-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f7aa-118">INPUTS</span></span>

### <span data-ttu-id="0f7aa-119">Keine</span><span class="sxs-lookup"><span data-stu-id="0f7aa-119">None</span></span>

## <span data-ttu-id="0f7aa-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f7aa-120">OUTPUTS</span></span>

### <span data-ttu-id="0f7aa-121">Microsoft. Azure. Commands. profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="0f7aa-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="0f7aa-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f7aa-122">NOTES</span></span>

## <span data-ttu-id="0f7aa-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f7aa-123">RELATED LINKS</span></span>
