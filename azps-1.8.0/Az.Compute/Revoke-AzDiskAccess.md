---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 6fe1fee57942c72b51382b6332df22993a9bb56e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820579"
---
# <span data-ttu-id="4556b-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="4556b-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="4556b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4556b-102">SYNOPSIS</span></span>
<span data-ttu-id="4556b-103">Widerruft einen Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="4556b-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="4556b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4556b-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4556b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4556b-105">DESCRIPTION</span></span>
<span data-ttu-id="4556b-106">Mit dem Cmdlet **REVOKE-AzDiskAccess** wird ein Zugriff auf einen Datenträger aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="4556b-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="4556b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4556b-107">EXAMPLES</span></span>

### <span data-ttu-id="4556b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4556b-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="4556b-109">Widerrufen des Zugriffs auf den Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="4556b-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="4556b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4556b-110">PARAMETERS</span></span>

### <span data-ttu-id="4556b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4556b-111">-AsJob</span></span>
<span data-ttu-id="4556b-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4556b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4556b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4556b-113">-DefaultProfile</span></span>
<span data-ttu-id="4556b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4556b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4556b-115">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="4556b-115">-DiskName</span></span>
<span data-ttu-id="4556b-116">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="4556b-116">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4556b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4556b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4556b-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4556b-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4556b-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4556b-119">-Confirm</span></span>
<span data-ttu-id="4556b-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4556b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4556b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4556b-121">-WhatIf</span></span>
<span data-ttu-id="4556b-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4556b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4556b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4556b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4556b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4556b-124">CommonParameters</span></span>
<span data-ttu-id="4556b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4556b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4556b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4556b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4556b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4556b-127">INPUTS</span></span>

### <span data-ttu-id="4556b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4556b-128">System.String</span></span>

## <span data-ttu-id="4556b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4556b-129">OUTPUTS</span></span>

### <span data-ttu-id="4556b-130">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4556b-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4556b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="4556b-131">NOTES</span></span>

## <span data-ttu-id="4556b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4556b-132">RELATED LINKS</span></span>
