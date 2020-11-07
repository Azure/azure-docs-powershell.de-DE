---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: b0f4e67630a3a762fe78c9438c6ae39f948404c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664452"
---
# <span data-ttu-id="d1501-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d1501-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="d1501-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1501-102">SYNOPSIS</span></span>
<span data-ttu-id="d1501-103">Löscht einen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d1501-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1501-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1501-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1501-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1501-105">DESCRIPTION</span></span>
<span data-ttu-id="d1501-106">Löscht einen Active Directory-Benutzer (Firmen-oder Schulkonto, auch bekannt als org-ID).</span><span class="sxs-lookup"><span data-stu-id="d1501-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="d1501-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1501-107">EXAMPLES</span></span>

### <span data-ttu-id="d1501-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1501-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d1501-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="d1501-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="d1501-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1501-110">PARAMETERS</span></span>

### <span data-ttu-id="d1501-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d1501-111">-Force</span></span>
<span data-ttu-id="d1501-112">Wenn angegeben, wird keine Bestätigung zum Löschen des Benutzers verlangt.</span><span class="sxs-lookup"><span data-stu-id="d1501-112">If specified, doesn't ask for confirmation for deleting user.</span></span>

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

### <span data-ttu-id="d1501-113">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="d1501-113">-UPNOrObjectId</span></span>
<span data-ttu-id="d1501-114">Der Benutzerprinzipalname oder die ObjectID des Benutzers, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1501-114">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1501-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1501-115">-Confirm</span></span>
<span data-ttu-id="d1501-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1501-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1501-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1501-117">-WhatIf</span></span>
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

### <span data-ttu-id="d1501-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1501-118">-DefaultProfile</span></span>
<span data-ttu-id="d1501-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1501-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1501-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1501-120">CommonParameters</span></span>
<span data-ttu-id="d1501-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1501-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1501-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1501-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1501-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1501-123">INPUTS</span></span>

## <span data-ttu-id="d1501-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1501-124">OUTPUTS</span></span>

## <span data-ttu-id="d1501-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1501-125">NOTES</span></span>

## <span data-ttu-id="d1501-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1501-126">RELATED LINKS</span></span>

[<span data-ttu-id="d1501-127">Neu – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d1501-127">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="d1501-128">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d1501-128">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="d1501-129">Satz-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d1501-129">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

