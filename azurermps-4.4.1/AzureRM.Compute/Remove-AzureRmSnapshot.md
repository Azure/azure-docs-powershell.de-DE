---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 4c7260d3c1131ab573bf933f4b83022cef20819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505149"
---
# <span data-ttu-id="73a2f-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="73a2f-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="73a2f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="73a2f-103">Entfernt einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="73a2f-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73a2f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73a2f-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73a2f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73a2f-105">DESCRIPTION</span></span>
<span data-ttu-id="73a2f-106">Das Cmdlet **Remove-AzureRmSnapshot** entfernt einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="73a2f-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="73a2f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73a2f-107">EXAMPLES</span></span>

### <span data-ttu-id="73a2f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="73a2f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="73a2f-109">Dieser Befehl entfernt den Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="73a2f-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="73a2f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="73a2f-110">PARAMETERS</span></span>

### <span data-ttu-id="73a2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a2f-111">-DefaultProfile</span></span>
<span data-ttu-id="73a2f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73a2f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73a2f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="73a2f-113">-Force</span></span>
<span data-ttu-id="73a2f-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="73a2f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="73a2f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73a2f-115">-ResourceGroupName</span></span>
<span data-ttu-id="73a2f-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="73a2f-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="73a2f-117">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="73a2f-117">-SnapshotName</span></span>
<span data-ttu-id="73a2f-118">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="73a2f-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="73a2f-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="73a2f-119">-Confirm</span></span>
<span data-ttu-id="73a2f-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73a2f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73a2f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73a2f-121">-WhatIf</span></span>
<span data-ttu-id="73a2f-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73a2f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73a2f-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73a2f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73a2f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a2f-124">CommonParameters</span></span>
<span data-ttu-id="73a2f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a2f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a2f-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a2f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a2f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73a2f-127">INPUTS</span></span>

### <span data-ttu-id="73a2f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="73a2f-128">System.String</span></span>

## <span data-ttu-id="73a2f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73a2f-129">OUTPUTS</span></span>

### <span data-ttu-id="73a2f-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="73a2f-130">System.Object</span></span>

## <span data-ttu-id="73a2f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="73a2f-131">NOTES</span></span>

## <span data-ttu-id="73a2f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73a2f-132">RELATED LINKS</span></span>

