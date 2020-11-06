---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bd9b47b54cb609a06da10488007f55d91d157b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501657"
---
# <span data-ttu-id="23f0f-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="23f0f-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="23f0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="23f0f-103">Ruft eine Liste der Vaults für Wiederherstellungsdienste ab.</span><span class="sxs-lookup"><span data-stu-id="23f0f-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23f0f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23f0f-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23f0f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="23f0f-106">Das Cmdlet " **Get-AzureRmRecoveryServicesVault** " Ruft eine Liste der Wiederherstellungsdienste-Tresore im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="23f0f-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="23f0f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23f0f-107">EXAMPLES</span></span>

## <span data-ttu-id="23f0f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="23f0f-108">PARAMETERS</span></span>

### <span data-ttu-id="23f0f-109">-Name</span><span class="sxs-lookup"><span data-stu-id="23f0f-109">-Name</span></span>
<span data-ttu-id="23f0f-110">Gibt den Namen des zu abfragenden Tresors an.</span><span class="sxs-lookup"><span data-stu-id="23f0f-110">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f0f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23f0f-111">-ResourceGroupName</span></span>
<span data-ttu-id="23f0f-112">Gibt den Namen der Azure-Ressourcengruppe an, in der erstellt werden soll, oder aus der das angegebene Wiederherstellungsdienste-Objekt abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="23f0f-112">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f0f-113">-DefaultProfile</span></span>
<span data-ttu-id="23f0f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23f0f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23f0f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f0f-115">CommonParameters</span></span>
<span data-ttu-id="23f0f-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f0f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f0f-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f0f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f0f-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23f0f-118">INPUTS</span></span>

## <span data-ttu-id="23f0f-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23f0f-119">OUTPUTS</span></span>

### <span data-ttu-id="23f0f-120">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. RecoveryServices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="23f0f-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="23f0f-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="23f0f-121">NOTES</span></span>

## <span data-ttu-id="23f0f-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23f0f-122">RELATED LINKS</span></span>

[<span data-ttu-id="23f0f-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="23f0f-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="23f0f-124">Neu – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="23f0f-124">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="23f0f-125">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="23f0f-125">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


