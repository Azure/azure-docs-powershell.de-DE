---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 735ea22547183b8047a3a32d0a147b428b39f630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502478"
---
# <span data-ttu-id="7e213-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7e213-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="7e213-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e213-102">SYNOPSIS</span></span>
<span data-ttu-id="7e213-103">Löscht einen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7e213-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e213-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e213-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e213-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e213-105">DESCRIPTION</span></span>
<span data-ttu-id="7e213-106">Löscht einen Active Directory-Benutzer (Firmen-oder Schulkonto, auch bekannt als org-ID).</span><span class="sxs-lookup"><span data-stu-id="7e213-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="7e213-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e213-107">EXAMPLES</span></span>

### <span data-ttu-id="7e213-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7e213-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7e213-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="7e213-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="7e213-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e213-110">PARAMETERS</span></span>

### <span data-ttu-id="7e213-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e213-111">-DefaultProfile</span></span>
<span data-ttu-id="7e213-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7e213-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e213-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7e213-113">-Force</span></span>
<span data-ttu-id="7e213-114">Wenn angegeben, wird keine Bestätigung zum Löschen des Benutzers verlangt.</span><span class="sxs-lookup"><span data-stu-id="7e213-114">If specified, doesn't ask for confirmation for deleting user.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e213-115">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="7e213-115">-UPNOrObjectId</span></span>
<span data-ttu-id="7e213-116">Der Benutzerprinzipalname oder die ObjectID des Benutzers, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e213-116">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e213-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7e213-117">-Confirm</span></span>
<span data-ttu-id="7e213-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e213-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e213-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e213-119">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e213-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e213-120">CommonParameters</span></span>
<span data-ttu-id="7e213-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e213-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e213-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e213-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e213-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e213-123">INPUTS</span></span>

### <span data-ttu-id="7e213-124">Keine</span><span class="sxs-lookup"><span data-stu-id="7e213-124">None</span></span>
<span data-ttu-id="7e213-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7e213-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e213-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e213-126">OUTPUTS</span></span>

## <span data-ttu-id="7e213-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e213-127">NOTES</span></span>

## <span data-ttu-id="7e213-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e213-128">RELATED LINKS</span></span>

[<span data-ttu-id="7e213-129">Neu – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7e213-129">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="7e213-130">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7e213-130">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="7e213-131">Satz-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7e213-131">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

