---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: a1b06a870822f2fef0bf2f9a39321c13642f8cad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505638"
---
# <span data-ttu-id="f7bf5-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f7bf5-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="f7bf5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="f7bf5-103">Gewährt einen Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="f7bf5-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7bf5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7bf5-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7bf5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="f7bf5-106">Das Cmdlet **Grant-AzureRmDiskAccess** gewährt einen Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="f7bf5-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="f7bf5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7bf5-107">EXAMPLES</span></span>

### <span data-ttu-id="f7bf5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7bf5-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="f7bf5-109">Gewähren Sie "Read"-Zugriff auf den Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" für 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f7bf5-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="f7bf5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7bf5-110">PARAMETERS</span></span>

### <span data-ttu-id="f7bf5-111">-Access</span><span class="sxs-lookup"><span data-stu-id="f7bf5-111">-Access</span></span>
<span data-ttu-id="f7bf5-112">Gibt die Zugriffsebene an.</span><span class="sxs-lookup"><span data-stu-id="f7bf5-112">Specifies Access level.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7bf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7bf5-113">-DefaultProfile</span></span>
<span data-ttu-id="f7bf5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7bf5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7bf5-115">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="f7bf5-115">-DiskName</span></span>
<span data-ttu-id="f7bf5-116">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="f7bf5-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="f7bf5-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="f7bf5-117">-DurationInSecond</span></span>
<span data-ttu-id="f7bf5-118">Gibt die Zugriffsdauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="f7bf5-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7bf5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7bf5-119">-ResourceGroupName</span></span>
<span data-ttu-id="f7bf5-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f7bf5-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f7bf5-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7bf5-121">-Confirm</span></span>
<span data-ttu-id="f7bf5-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7bf5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7bf5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7bf5-123">-WhatIf</span></span>
<span data-ttu-id="f7bf5-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7bf5-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7bf5-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7bf5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7bf5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7bf5-126">CommonParameters</span></span>
<span data-ttu-id="f7bf5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7bf5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7bf5-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7bf5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7bf5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7bf5-129">INPUTS</span></span>

### <span data-ttu-id="f7bf5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f7bf5-130">System.String</span></span>

## <span data-ttu-id="f7bf5-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7bf5-131">OUTPUTS</span></span>

### <span data-ttu-id="f7bf5-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="f7bf5-132">System.Object</span></span>

## <span data-ttu-id="f7bf5-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7bf5-133">NOTES</span></span>

## <span data-ttu-id="f7bf5-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7bf5-134">RELATED LINKS</span></span>

