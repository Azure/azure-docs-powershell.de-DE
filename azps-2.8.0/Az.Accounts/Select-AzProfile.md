---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 35b15fab6888a300fcef9f80b05aa034a9f07ce3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658435"
---
# <span data-ttu-id="f2cab-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="f2cab-101">Select-AzProfile</span></span>

## <span data-ttu-id="f2cab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2cab-102">SYNOPSIS</span></span>
<span data-ttu-id="f2cab-103">Für Module, die mehrere Dienstprofile unterstützen, laden Sie die Cmdlets, die dem angegebenen Dienstprofil entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f2cab-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="f2cab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2cab-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2cab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2cab-105">DESCRIPTION</span></span>
<span data-ttu-id="f2cab-106">Für Module, die mehrere Dienstprofile unterstützen, laden Sie die Cmdlets, die dem angegebenen Dienstprofil entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f2cab-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="f2cab-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2cab-107">EXAMPLES</span></span>

### <span data-ttu-id="f2cab-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f2cab-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="f2cab-109">Laden Sie Cmdlets für das AzureStack-Profil ab März 2019</span><span class="sxs-lookup"><span data-stu-id="f2cab-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="f2cab-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2cab-110">PARAMETERS</span></span>

### <span data-ttu-id="f2cab-111">-Name</span><span class="sxs-lookup"><span data-stu-id="f2cab-111">-Name</span></span>
<span data-ttu-id="f2cab-112">Der Name des Profils, das Sie auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="f2cab-112">The name of the profile to select</span></span>

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

### <span data-ttu-id="f2cab-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2cab-113">-PassThru</span></span>
<span data-ttu-id="f2cab-114">Wenn vorhanden, erzwingt das Cmdlet, bei erfolgreicher Ausführung einen Wert zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="f2cab-114">When present, forces the cmdlet to return a value on successful execution</span></span>

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

### <span data-ttu-id="f2cab-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f2cab-115">-Confirm</span></span>
<span data-ttu-id="f2cab-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2cab-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2cab-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2cab-117">-WhatIf</span></span>
<span data-ttu-id="f2cab-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2cab-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2cab-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2cab-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2cab-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2cab-120">CommonParameters</span></span>
<span data-ttu-id="f2cab-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2cab-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2cab-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2cab-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2cab-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2cab-123">INPUTS</span></span>

### <span data-ttu-id="f2cab-124">Keine</span><span class="sxs-lookup"><span data-stu-id="f2cab-124">None</span></span>

## <span data-ttu-id="f2cab-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2cab-125">OUTPUTS</span></span>

### <span data-ttu-id="f2cab-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="f2cab-126">System.Object</span></span>
## <span data-ttu-id="f2cab-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2cab-127">NOTES</span></span>

## <span data-ttu-id="f2cab-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2cab-128">RELATED LINKS</span></span>
