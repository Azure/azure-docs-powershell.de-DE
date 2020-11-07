---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
ms.openlocfilehash: bbde391c56d4b50320f15441b75b93d125771ccb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850912"
---
# <span data-ttu-id="8805b-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="8805b-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="8805b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8805b-102">SYNOPSIS</span></span>
<span data-ttu-id="8805b-103">Widerruft einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="8805b-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8805b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8805b-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8805b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8805b-105">DESCRIPTION</span></span>
<span data-ttu-id="8805b-106">Das **REVOKE-AzureRmSnapshotAccess-** Cmdlet widerruft einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="8805b-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="8805b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8805b-107">EXAMPLES</span></span>

### <span data-ttu-id="8805b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8805b-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="8805b-109">Widerrufen des Zugriffs auf den Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="8805b-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="8805b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8805b-110">PARAMETERS</span></span>

### <span data-ttu-id="8805b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8805b-111">-AsJob</span></span>
<span data-ttu-id="8805b-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8805b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8805b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8805b-113">-DefaultProfile</span></span>
<span data-ttu-id="8805b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8805b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8805b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8805b-115">-ResourceGroupName</span></span>
<span data-ttu-id="8805b-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8805b-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8805b-117">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="8805b-117">-SnapshotName</span></span>
<span data-ttu-id="8805b-118">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="8805b-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8805b-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8805b-119">-Confirm</span></span>
<span data-ttu-id="8805b-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8805b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8805b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8805b-121">-WhatIf</span></span>
<span data-ttu-id="8805b-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8805b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8805b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8805b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8805b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8805b-124">CommonParameters</span></span>
<span data-ttu-id="8805b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8805b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8805b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8805b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8805b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8805b-127">INPUTS</span></span>

### <span data-ttu-id="8805b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8805b-128">System.String</span></span>

## <span data-ttu-id="8805b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8805b-129">OUTPUTS</span></span>

### <span data-ttu-id="8805b-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="8805b-130">System.Object</span></span>

## <span data-ttu-id="8805b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="8805b-131">NOTES</span></span>

## <span data-ttu-id="8805b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8805b-132">RELATED LINKS</span></span>

