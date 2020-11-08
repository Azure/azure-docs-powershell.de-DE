---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 1ca2244d4ed1a47535a228ed772d9d9a6ecb6acb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995923"
---
# <span data-ttu-id="aead7-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="aead7-101">Select-AzProfile</span></span>

## <span data-ttu-id="aead7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aead7-102">SYNOPSIS</span></span>
<span data-ttu-id="aead7-103">Für Module, die mehrere Dienstprofile unterstützen, laden Sie die Cmdlets, die dem angegebenen Dienstprofil entsprechen.</span><span class="sxs-lookup"><span data-stu-id="aead7-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="aead7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aead7-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aead7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aead7-105">DESCRIPTION</span></span>
<span data-ttu-id="aead7-106">Für Module, die mehrere Dienstprofile unterstützen, laden Sie die Cmdlets, die dem angegebenen Dienstprofil entsprechen.</span><span class="sxs-lookup"><span data-stu-id="aead7-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="aead7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aead7-107">EXAMPLES</span></span>

### <span data-ttu-id="aead7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aead7-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="aead7-109">Laden Sie Cmdlets für das AzureStack-Profil ab März 2019</span><span class="sxs-lookup"><span data-stu-id="aead7-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="aead7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aead7-110">PARAMETERS</span></span>

### <span data-ttu-id="aead7-111">-Name</span><span class="sxs-lookup"><span data-stu-id="aead7-111">-Name</span></span>
<span data-ttu-id="aead7-112">Der Name des Profils, das Sie auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="aead7-112">The name of the profile to select</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProfileName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aead7-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aead7-113">-PassThru</span></span>
<span data-ttu-id="aead7-114">Wenn vorhanden, erzwingt das Cmdlet, bei erfolgreicher Ausführung einen Wert zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="aead7-114">When present, forces the cmdlet to return a value on successful execution</span></span>

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

### <span data-ttu-id="aead7-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aead7-115">-Confirm</span></span>
<span data-ttu-id="aead7-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aead7-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aead7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aead7-117">-WhatIf</span></span>
<span data-ttu-id="aead7-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aead7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aead7-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aead7-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aead7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aead7-120">CommonParameters</span></span>
<span data-ttu-id="aead7-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aead7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aead7-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aead7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aead7-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aead7-123">INPUTS</span></span>

### <span data-ttu-id="aead7-124">Keine</span><span class="sxs-lookup"><span data-stu-id="aead7-124">None</span></span>

## <span data-ttu-id="aead7-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aead7-125">OUTPUTS</span></span>

### <span data-ttu-id="aead7-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="aead7-126">System.Object</span></span>
## <span data-ttu-id="aead7-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="aead7-127">NOTES</span></span>

## <span data-ttu-id="aead7-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aead7-128">RELATED LINKS</span></span>
