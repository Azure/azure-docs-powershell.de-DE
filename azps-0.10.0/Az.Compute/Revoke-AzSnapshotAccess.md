---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 4c22f8cf7ded27083ad6f1ddbd5994241d542c0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844320"
---
# <span data-ttu-id="1e696-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="1e696-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="1e696-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e696-102">SYNOPSIS</span></span>
<span data-ttu-id="1e696-103">Widerruft einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="1e696-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="1e696-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e696-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e696-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e696-105">DESCRIPTION</span></span>
<span data-ttu-id="1e696-106">Das **REVOKE-AzSnapshotAccess-** Cmdlet widerruft einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="1e696-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="1e696-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e696-107">EXAMPLES</span></span>

### <span data-ttu-id="1e696-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1e696-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="1e696-109">Widerrufen des Zugriffs auf den Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="1e696-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="1e696-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e696-110">PARAMETERS</span></span>

### <span data-ttu-id="1e696-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e696-111">-AsJob</span></span>
<span data-ttu-id="1e696-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1e696-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e696-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e696-113">-DefaultProfile</span></span>
<span data-ttu-id="1e696-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e696-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e696-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e696-115">-ResourceGroupName</span></span>
<span data-ttu-id="1e696-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1e696-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1e696-117">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="1e696-117">-SnapshotName</span></span>
<span data-ttu-id="1e696-118">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="1e696-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="1e696-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e696-119">-Confirm</span></span>
<span data-ttu-id="1e696-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e696-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e696-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e696-121">-WhatIf</span></span>
<span data-ttu-id="1e696-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e696-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e696-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e696-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e696-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e696-124">CommonParameters</span></span>
<span data-ttu-id="1e696-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e696-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e696-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e696-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e696-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e696-127">INPUTS</span></span>

### <span data-ttu-id="1e696-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1e696-128">System.String</span></span>

## <span data-ttu-id="1e696-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e696-129">OUTPUTS</span></span>

### <span data-ttu-id="1e696-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="1e696-130">System.Object</span></span>

## <span data-ttu-id="1e696-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e696-131">NOTES</span></span>

## <span data-ttu-id="1e696-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e696-132">RELATED LINKS</span></span>

