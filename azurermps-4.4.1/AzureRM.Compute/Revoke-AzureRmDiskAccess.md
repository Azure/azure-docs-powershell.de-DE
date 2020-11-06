---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 58cbbfd2314589fd6b28f2ff375aa268c39e63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477266"
---
# <span data-ttu-id="1c7e6-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="1c7e6-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="1c7e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c7e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1c7e6-103">Widerruft einen Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="1c7e6-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c7e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c7e6-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c7e6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c7e6-105">DESCRIPTION</span></span>
<span data-ttu-id="1c7e6-106">Mit dem Cmdlet **REVOKE-AzureRmDiskAccess** wird ein Zugriff auf einen Datenträger aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="1c7e6-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="1c7e6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c7e6-107">EXAMPLES</span></span>

### <span data-ttu-id="1c7e6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1c7e6-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="1c7e6-109">Widerrufen des Zugriffs auf den Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="1c7e6-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="1c7e6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c7e6-110">PARAMETERS</span></span>

### <span data-ttu-id="1c7e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c7e6-111">-DefaultProfile</span></span>
<span data-ttu-id="1c7e6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1c7e6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c7e6-113">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="1c7e6-113">-DiskName</span></span>
<span data-ttu-id="1c7e6-114">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="1c7e6-114">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c7e6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c7e6-115">-ResourceGroupName</span></span>
<span data-ttu-id="1c7e6-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1c7e6-116">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c7e6-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c7e6-117">-Confirm</span></span>
<span data-ttu-id="1c7e6-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c7e6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c7e6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c7e6-119">-WhatIf</span></span>
<span data-ttu-id="1c7e6-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c7e6-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c7e6-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c7e6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c7e6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c7e6-122">CommonParameters</span></span>
<span data-ttu-id="1c7e6-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c7e6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c7e6-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c7e6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c7e6-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c7e6-125">INPUTS</span></span>

### <span data-ttu-id="1c7e6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1c7e6-126">System.String</span></span>

## <span data-ttu-id="1c7e6-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c7e6-127">OUTPUTS</span></span>

### <span data-ttu-id="1c7e6-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="1c7e6-128">System.Object</span></span>

## <span data-ttu-id="1c7e6-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c7e6-129">NOTES</span></span>

## <span data-ttu-id="1c7e6-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c7e6-130">RELATED LINKS</span></span>

